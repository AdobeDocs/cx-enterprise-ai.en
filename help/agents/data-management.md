---
title: Data Management Agent for Adobe Experience Platform
description: Learn how to use the Data Management Agent in CX Coworker to find and analyze Adobe Experience Platform datasets and manage data lake retention policies.
---
# Data Management Agent

>[!AVAILABILITY]
>
>The Data Management Agent is available to all customers with access to Adobe CX Enterprise Coworker.

To understand and manage data lake retention for your Experience Event datasets, use the Data Management Agent in CX Coworker. As Experience Event datasets in your Adobe Experience Platform data lake grow, queries and downstream processes can take longer to complete, while retention requirements become harder to manage. Describe what you want to accomplish in natural language. The Data Management Agent finds the relevant Experience Event datasets, analyzes how actively they're used, and models how much data a proposed retention period would affect. When you're ready to act, it helps you set, change, or remove a retention policy and asks for your confirmation before anything changes.

## What the Data Management Agent can do {#what-the-data-management-agent-can-do}

The Data Management Agent provides four skills.

>[!NOTE]
>
>The List datasets, Analyze dataset usage, and Analyze dataset retention skills are read only. Only the Manage dataset retention skill can change a data lake retention policy, and it requires your explicit confirmation before applying any change.

| Skill | Description |
|---|---|
| **List datasets** | Use when deciding where to start a retention review. Lists your Experience Event datasets with storage size, row count, existing retention settings, and Profile enablement so you can quickly identify datasets that may be candidates for a data lake retention policy |
| **Analyze dataset usage** | Use before deciding whether a dataset is a good candidate for a data lake retention policy. Classifies how actively a specific dataset is used based on signals such as recent ingestion, query activity, and downstream application usage. |
| **Analyze dataset retention** | Use before committing to a retention period. Shows a dataset's storage metrics and the age of its data, then uses that age distribution to approximate how much data a potential retention period would keep or remove. |
| **Manage dataset retention** | Use when you're ready to act. Sets, changes, or removes a data lake retention policy on a dataset, with an impact preview and confirmation before anything changes. |

## Scope: data lake retention vs. other data management tools {#scope}

Use the Data Management Agent when you need to find and analyze Experience Event datasets and set, change, or remove a data lake retention policy.

If you're not sure whether a data lake retention policy is the right option for your goal, see [Choose the right data lifecycle management capability](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/choose-a-capability) to compare the available retention and deletion options.

These skills don't manage the following related capabilities:

- **Profile store retention policy.** To manage how long Experience Events remain in the Profile store, configure an Experience Event expiration policy on Profile-enabled Experience Event datasets. See [Experience Event expiration](https://experienceleague.adobe.com/en/docs/experience-platform/profile/event-expirations).
- **Sandbox-wide pseudonymous profile data expiration.** To automatically delete pseudonymous profile data across a sandbox once it meets the configured conditions, see [Pseudonymous profiles](https://experienceleague.adobe.com/en/docs/experience-platform/profile/pseudonymous-profiles).
- **Dataset expiration.** To schedule an entire dataset for deletion on a future date, see [Dataset expiration](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/ui/dataset-expiration).
- **Record Delete.** To remove individual profile records for privacy or hygiene reasons, see [Record Delete](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/ui/record-delete).

## Prerequisites {#prerequisites}

Before you begin, ensure that you have:

- Access to Adobe Experience Platform and the sandbox that contains the datasets you want to review.
- The Adobe Experience Platform permissions required for the datasets and retention actions you want to use. The Data Management Agent uses your existing Experience Platform permissions and does not grant additional access. See the [Access control overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home) for how Adobe Experience Platform permissions and roles work.
- The Adobe CXO plugin installed in CX Coworker.

For instructions on installing plugins, see the [Coworker UI guide](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide).

## Use the Data Management Agent {#use-the-data-management-agent}

Interact with the Data Management Agent through CX Coworker using natural language. Describe your goal, then refine the results with follow-up questions.

>[!NOTE]
>
>Before you begin, make sure you're working in the sandbox that contains the datasets you want to review.

To use the Data Management Agent:

1. Navigate to **[!UICONTROL CX Coworker]**. For access details, see the [Coworker UI guide](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide).
1. Enter a request that describes what you want to accomplish.
1. Review the results and use follow-up questions to continue your investigation.

If a request changes a data lake retention policy, the Data Management Agent shows the proposed impact and requires your confirmation before applying the change.

For an end-to-end workflow for identifying datasets, analyzing usage and retention impact, and managing data lake retention policies, see [Manage data lake retention](../coworker/chat/use-cases/data-management/manage-data-lake-retention.md).

## How the Data Management Agent works {#how-the-data-management-agent-works}

The Data Management Agent uses deterministic calculations to analyze dataset usage, so the same inputs produce the same usage tier. It also calculates retention impact programmatically rather than relying on AI-generated estimates. Retention impact remains an approximation because it is based on the age distribution of the data. The agent retrieves data directly from Adobe Experience Platform services to provide current information about your datasets.

## Limitations {#limitations}

The Data Management Agent can identify datasets that may be good candidates for a data lake retention policy, but it does not decide whether a dataset requires one. It does not apply, change, or remove a retention policy without your explicit confirmation.

## Next steps {#next-steps}

After reading this guide, you should understand how to use the Data Management Agent in CX Coworker to find, analyze, and manage data lake retention on your Experience Event datasets.

For more information about how data lake retention policies work in Adobe Experience Platform, including retention behavior and configuration, see [Experience Event dataset retention (TTL) guide](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/experience-event-dataset-retention-ttl-guide).
