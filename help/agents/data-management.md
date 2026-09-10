---
title: Data Management Agentic Skills
description: Learn how to use Data Management Agentic Skills in CX Coworker to find, analyze, and manage data-lake retention (TTL) on your Adobe Experience Platform datasets through natural-language conversations.
---

# Data Management Agentic Skills

>[!AVAILABILITY]
>
>Data Management Agentic Skills are available to all customers with access to Adobe CX Enterprise Coworker.
>
>To use Data Management Agentic Skills, you must have access to the Adobe Experience Platform sandbox that contains the datasets you want to review. Changing a retention policy requires permission to modify dataset retention settings in that sandbox.

<!-- TODO(author): Confirm the exact AEP permission/role name(s) required for each skill with the engineering owner before publishing. See execution-brief.md, U5. Also confirm before publishing that all four skills described in this guide are generally available; as of the kickoff meeting, one skill depended on an MCP server pending an ARB review (see execution-brief.md, U4, and the related TODO under Limitations). -->

As datasets in your Adobe Experience Platform data lake grow, queries and downstream applications that depend on them slow down, and staying on top of data retention requirements becomes harder. To manage data-lake retention without writing queries or reviewing dataset details manually, use Data Management Agentic Skills in CX Coworker. Describe what you want to accomplish in natural language, and the agent finds the relevant Customer Event datasets, analyzes how they're used, and helps you set, change, or remove a retention policy — always previewing the impact and asking for your confirmation before anything changes.

## What Data Management Agentic Skills can do {#what-data-management-agentic-skills-can-do}

Data Management Agentic Skills cover four related capabilities.

| Skill | Description |
|---|---|
| **List datasets** | Lists your Customer Event datasets with storage size, row count, existing retention settings, and profile enablement, so you can find retention candidates quickly. |
| **Analyze dataset usage** | Classifies how actively a specific dataset is used, based on signals such as recent ingestion, query activity, and downstream application usage. |
| **Analyze dataset retention** | Shows a dataset's storage metrics and the age of the data it contains, and models, as an approximation based on that age distribution, how much data a candidate retention period would keep or remove. |
| **Manage dataset retention** | Sets, changes, or removes a data-lake retention (TTL) policy on a dataset, with an impact preview and confirmation before anything changes. |

## Scope: data-lake retention vs. other data management tools {#scope}

Data Management Agentic Skills manage data-lake retention — also called Experience Event TTL — on Customer Event (time-series) datasets. Use these skills to find, analyze, and set retention on the datasets that make up your data lake.

These skills don't manage the following related capabilities:

- **Profile store retention.** To manage how long profile data is retained in Real-Time Customer Profile, apply profile event retention on Profile-enabled time-series datasets. See [Profile event retention](https://experienceleague.adobe.com/en/docs/experience-platform/profile/event-expirations).
- **Sandbox-wide pseudonymous profile TTL.** See [Pseudonymous profiles](https://experienceleague.adobe.com/en/docs/experience-platform/profile/pseudonymous-profiles).
- **Dataset expiration.** To schedule an entire dataset for deletion on a future date, see [Dataset expiration](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/ui/dataset-expiration).
- **Record Delete.** To remove individual profile records for privacy or hygiene reasons, see [Record Delete](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/ui/record-delete).

## Prerequisites {#prerequisites}

Before you begin, ensure that you have:

- Access to Adobe Experience Platform and the sandbox that contains the datasets you want to review.
- Permission to view the dataset catalog and, if you plan to set, change, or remove a retention policy, permission to modify dataset retention settings.
- The Adobe CXO plugin installed in CX Coworker.

For instructions on installing plugins, see the [Coworker UI guide](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide).

## Use Data Management Agentic Skills {#use-data-management-agentic-skills}

Interact with Data Management Agentic Skills through CX Coworker using natural language. Describe your goal as clearly as possible, then refine the results with follow-up questions.

To use Data Management Agentic Skills:

1. Navigate to **[!UICONTROL CX Coworker]**.
1. Enter a request. For example:

   *"Show me my largest event datasets."*

1. Review the results.
1. Ask a follow-up question to narrow your analysis. For example:

   *"How actively is this dataset being used?"*

1. To set, change, or remove a retention policy, review the impact preview that Data Management Agentic Skills return, then confirm the request before it's applied.

## Supported use cases {#supported-use-cases}

Data Management Agentic Skills support two kinds of work: exploring and analyzing your datasets, and managing retention policies on them.

### Find your largest datasets {#find-your-largest-datasets}

Use the List datasets skill to surface Customer Event datasets by storage size, row count, existing retention status, and profile enablement. Use this skill as your starting point for a retention review, then filter by criteria such as dataset size or row count to narrow the list. This skill is read-only. Coworker returns these datasets as a table you can scan and compare, along with visualizations that help you see which datasets stand out by size, row count, or data age.

Not every unused or abandoned dataset that this skill surfaces is automatically a candidate for a data-lake retention (TTL) policy — some may be better suited to [Dataset expiration](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/ui/dataset-expiration) instead. Confirm that a dataset is a Customer Event (time-series) dataset before setting a retention policy on it.

For example:

- "Show me my largest event datasets."
- "Show me datasets larger than 100 GB that don't have data lake retention set."
- "I need to remove about 2 TBs of data. Where should I start?"
- "Can you help me find data that's orphaned, abandoned, or unused?"
- "Prioritize datasets with no access in the last 90 days."

### Check how actively a dataset is used {#check-how-actively-a-dataset-is-used}

Use the Analyze dataset usage skill to understand how actively a specific dataset is used. The skill evaluates nine deterministic signals — for example, recent ingestion activity, query activity, schema stability, and whether the dataset feeds other Adobe Experience Platform applications — then classifies the dataset into a usage tier. This skill is read-only. Coworker returns the resulting usage tier along with a breakdown of the underlying signals and a plain-language summary of what they indicate about the dataset.

<!-- TODO(author): Confirm final usage-tier names and thresholds with engineering before publishing. Both the tier labels and the day-based thresholds behind them were still under discussion as of the kickoff meeting. See execution-brief.md, U2 and U3. -->

For example:

- "How actively is my Web Events dataset being used?"

### Deep dive into a dataset's retention posture {#deep-dive-into-a-datasets-retention-posture}

Use the Analyze dataset retention skill to review a dataset's storage metrics and the age distribution of the data it contains, and to model, as an approximation based on that age distribution, how much data a candidate retention period would keep or remove — by row count and storage size — before you commit to a change. This skill is read-only. Coworker returns this data-age and impact analysis directly in the conversation, so you can compare it against the dataset's current retention status before deciding whether to change it.

For example:

- "What would be the impact if I set a 60-day retention period on this dataset?"

### Set, change, or remove a retention policy {#set-change-or-remove-a-retention-policy}

Use the Manage dataset retention skill to set, change, or remove a data-lake retention (TTL) policy on a dataset. Before anything changes, the skill shows you an impact preview and asks you to confirm the request.

>[!IMPORTANT]
>
>The minimum data-lake retention period is 30 days; shorter periods aren't supported.

After you confirm a retention policy, the Adobe Experience Platform UI may take a short time to reflect the change. Removal of expired data is a separate process: data older than the retention period isn't purged instantly, but during a scheduled purge run that, in product demonstrations, typically completed within about 24 hours of confirmation. Every retention change — setting, changing, or removing a policy — is recorded in an audit trail that includes who made the change and when, which you can review directly in the Adobe Experience Platform audit log, with a link back to the relevant Adobe Experience Platform screen where available.

For example:

- "Set the retention on this dataset to 60 days."
- "Remove the retention policy on this dataset."

## How Data Management Agentic Skills work {#how-data-management-agentic-skills-work}

Data Management Agentic Skills calculate usage classifications using deterministic formulas rather than AI-generated estimates, so the same inputs always produce the same usage tier. Retention-impact modeling is also calculated programmatically rather than through AI-generated estimates, but it's an approximation based on the dataset's data-age distribution rather than an exact measurement. The skills read data directly from Adobe Experience Platform services rather than a delayed or cached copy, so the information you see reflects the current state of your sandbox.

## Best practices {#best-practices}

Keep the following practices in mind when using Data Management Agentic Skills:

- **Start with discovery.** Use the List datasets skill to review your largest datasets, and any that appear unused or abandoned, before you deep-dive into any single dataset.
- **Review the impact preview before you confirm.** Setting or changing a retention policy results in data being purged; review what would be kept and removed before you confirm the request.
- **Allow time for the change to appear.** After you confirm a retention change in CX Coworker, allow a short time for the Adobe Experience Platform UI to reflect it.

## Limitations {#limitations}

Keep the following constraints in mind when using Data Management Agentic Skills:

- Data Management Agentic Skills recommend retention candidates; they don't decide or apply a retention policy without your explicit confirmation.
- The minimum supported data-lake retention period is 30 days.
- A confirmed retention change is enforced during the next scheduled purge run, not instantly.

<!-- TODO(author): Confirm that all four skills are generally available at publication time. As of the kickoff meeting, migration to production was still in progress and one skill depended on an MCP server pending an ARB review. See execution-brief.md, U4. -->

## Next steps {#next-steps}

After reading this guide, you should understand how to use Data Management Agentic Skills in CX Coworker to find, analyze, and manage data-lake retention on your Customer Event datasets.

For more information, see the [Experience Event dataset retention (TTL) guide](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/experience-event-dataset-retention-ttl-guide).
