---
title: Validate Your Experience Platform Data with Coworker
description: Learn how to use the CX Enterprise Coworker data validation skill to check the quality of your Adobe Experience Platform datasets and fields through chat.
feature: AI Tools
role: User
level: Intermediate
doc-type: Tutorial
last-substantial-update: 2026-08-27T00:00:00.000Z
jira: PLAT-302857
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---

# Validate your Experience Platform data with Coworker

Coworker includes the Data Validation skill, which checks the data quality of your Experience Platform datasets. Use it to run statistical and semantic validations on datasets, analyze dataset fields, and identify data quality issues, all through a single Coworker Chat conversation.

Data engineers, data admins, and implementation engineers use it for rapid quality checks, without SQL queries or complex schema hierarchies.

Use this skill to:

* Validate key identity and event fields after a new implementation or an implementation update.
* Investigate a suspected mapping issue by inspecting a field's top values and invalid values.
* Run ongoing data stewardship checks on critical datasets to catch regressions early.

<!--TODO: skill display name "Data Validation skill" confirmed via the published KT-22622 video page (validate-dataset-quality-for-cja.md, merged 2026-09-16). Still need the technical skill ID from engineering (Petru Adrian Snep) for the use-cases overview table row. That page didn't add one either.-->

>[!NOTE]
>
>This skill is read-only. It doesn't change your data, schemas, or mappings.

## Before you begin

To validate your data with Coworker, you need:

* The name or ID of the dataset you want to validate.
* (Optional) The name of a specific field to validate, if you don't want the skill to select fields automatically.

## Start a validation session

1. Sign in to Coworker.

1. Select [!UICONTROL **New Chat**].

1. In the text field, prompt the agent to validate a field or a dataset. For example:

   **Prompt**

   > Validate the dataset Electronics Sample 1000.

   >[!TIP]
   >
   >Prepend your dataset name with the word "dataset" so the skill can identify it correctly. For example, use "Validate the dataset Electronics Sample 1000" instead of "Validate Electronics Sample 1000."

   Your request is routed to the Data Validation skill, which analyzes a sample of your dataset and returns results in the same conversation.

1. (Conditional) If the skill can't uniquely identify the dataset or field you mean, answer the clarifying question it asks, then continue.

   <!--TODO: confirm with engineering whether/how this disambiguation flow surfaces to the user. AN-457440 calls out "Platform API lookup disambiguation" as the one functional change over the AOv1 version (fixing malformed-input lookup failures), but the design doc doesn't describe the resulting UX. Verify with a live demo before publishing, and replace this bullet with the actual behavior (or remove it if there's no user-visible prompt).-->

## Choose what to validate

You can validate a single field or an entire dataset.

>[!BEGINTABS]

>[!TAB Field validation]

Validate a specific field in a dataset. This option provides:

* Null count and unique value count.
* Top unique values and their frequencies.
* AI-assisted semantic validation that flags values which don't match the field's expected format, based on the field's metadata and its actual values.

Example prompts:

* Validate the email field in the Customers_2024 dataset.
* Validate field status for the dataset customer_events_2024.
* Validate field person.address.city for Customer Data dataset.

>[!TAB Dataset validation]

Validate up to five fields in a dataset at once. You can specify the fields yourself, or let the skill analyze the dataset and automatically select the most relevant fields. This option returns the same information as field validation, across every field you validate.

Example prompts:

* Validate Customer Data 2024 dataset.
* Validate fields email, phone for Customers_2024.
* Summarize firstName, lastName, birthDate for Customer Data.

>[!ENDTABS]

## Review the results

<!--TODO: this section carries over the AOv1 output format from the previous AI Assistant experience (help/agents/data-validation.md), since AN-457440 states the Coworker skill maintains full feature parity with no UI/UX redesign. Replace with actual Coworker screenshots and confirm [!UICONTROL] labels once the Coworker rendering is available (design doc notes dataset validation rendering was still in development at the time of writing).-->

For each validated field, the skill returns:

**Basic statistics**

* Total row count used for the sample.
* Null count (and percentage null).
* Unique value count, where available.
* Top unique values and their frequencies.

**Semantic validation**

* A list of suspected invalid values.
* An explanation for each invalid value, for example "not a valid email format" or "timestamp outside expected range."

**Natural language summary**

* A short narrative summary of field quality.
* Suggested next actions, such as "review mapping for field X," "consider dropping field Y due to high null rate," or "tighten validation for email format."

| Aspect | Example output |
| --- | --- |
| Completeness | `nullCount = 9,532 (95.3%)` |
| Uniqueness | `uniqueCount = 3` |
| Top values | `"True" (255), "False" (243)` |
| Invalid values | `"abc@", reason: "not a valid email address"` |

## Checks performed by data validation

* **Completeness checks**: null and missing counts and percentages.
* **Distribution checks**: top unique values and their distributions, and high cardinality detection.
* **Semantic checks against the schema**: uses the XDM field name, type, and description to infer what a valid value looks like, then flags anomalies.
* **Datatype-aware checks**, where applicable:
  * Email: format and domain plausibility.
  * Phone: format readiness, for example E.164.
  * Dates and timestamps: basic format checks, for example ISO-8601.

These checks combine deterministic statistics with LLM-assisted semantic validation to detect values that look wrong even when they technically match the schema.

## Limitations

Before you validate your data, keep the following limitations in mind. These constraints balance performance with functionality and set expectations for the analysis and insights you can expect.

* **Sampling only**: the skill validates a sample of the dataset (typically the most recent 1,000 rows), not the entire dataset. Full-dataset scans aren't available.
* **Field count limit**: when you validate a dataset, the skill analyzes up to five fields per request. You can specify these fields, or let the skill select them automatically.
* **Probabilistic semantics**: detection of invalid values relies in part on LLM-based inference, which can occasionally miss subtle errors or flag borderline values.
* **Read-only**: the skill doesn't change your data or its schema. It highlights potential issues but doesn't perform automated fixes.

If your validation needs are more exhaustive or require complex business logic, supplement these results with additional tools such as Query Service or Data Prep validations.

## Related information

* [Validate AA to CJA data when upgrading](./data-validation-aa-cja.md)
* [Validate Customer Journey Analytics data with the Data Validation skill in Coworker](./validate-dataset-quality-for-cja.md)
* [Validate your data (AI Assistant)](/help/agents/data-validation.md)
