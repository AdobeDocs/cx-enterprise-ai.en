---
title: Data Management Agent for Adobe Experience Platform
description: Learn how to use the Data Management Agent in CX Coworker to find and analyze Adobe Experience Platform datasets and manage data-lake retention policies.
---
# Data Management Agent

>[!AVAILABILITY]
>
>The Data Management Agent is available to all customers with access to Adobe CX Enterprise Coworker.

<!-- TODO(author): Confirm with the PM/engineering owner whether the AEP "View Datasets" and "Manage Datasets" permissions (https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home) are the permissions that actually gate the read-only and mutating Data Management skills, respectively, or whether different permissions apply. See execution-brief.md, U5. Also confirm before publishing that all four skills described in this guide are generally available; as of the kickoff meeting, one skill depended on an MCP server pending an ARB review (see execution-brief.md, U4, and the related TODO under Limitations). -->

To understand and manage data-lake retention for your Experience Event datasets, use the Data Management Agent in CX Coworker. As datasets in your Adobe Experience Platform data lake grow, queries and downstream applications that depend on them can slow down, and managing data retention requirements becomes harder. Describe what you want to accomplish in natural language. The Data Management Agent finds the relevant Experience Event datasets, analyzes how actively they're used, and models how much data a candidate retention period would affect. When you're ready to act, it helps you set, change, or remove a retention policy and asks for your confirmation before anything changes.

## What the Data Management Agent can do {#what-the-data-management-agent-can-do}

The Data Management Agent provides four skills.

| Skill | Description |
|---|---|
| **List datasets** | Use when deciding where to start a retention review. Lists your Experience Event datasets with storage size, row count, existing retention settings, and profile enablement so you can quickly identify retention candidates. |
| **Analyze dataset usage** | Use before deciding whether a dataset is a good retention candidate. Classifies how actively a specific dataset is used based on signals such as recent ingestion, query activity, and downstream application usage. |
| **Analyze dataset retention** | Use before committing to a retention period. Shows a dataset's storage metrics and the age of its data, then models, as an approximation based on that age distribution, how much data a candidate retention period would keep or remove. |
| **Manage dataset retention** | Use when you're ready to act. Sets, changes, or removes a data lake retention policy on a dataset, with an impact preview and confirmation before anything changes. |

## Scope: data-lake retention vs. other data management tools {#scope}

Use the Data Management Agent when you need to find and analyze Experience Event datasets and set, change, or remove a data lake retention policy.

These skills don't manage the following related capabilities:

- **Profile store retention.** To manage how long profile data is retained in Real-Time Customer Profile, apply profile event retention on Profile-enabled time-series datasets. See [Profile event retention](https://experienceleague.adobe.com/en/docs/experience-platform/profile/event-expirations).
- **Sandbox-wide pseudonymous profile TTL.** To automatically delete pseudonymous profile data across a sandbox once it meets the configured conditions, see [Pseudonymous profiles](https://experienceleague.adobe.com/en/docs/experience-platform/profile/pseudonymous-profiles).
- **Dataset expiration.** To schedule an entire dataset for deletion on a future date, see [Dataset expiration](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/ui/dataset-expiration).
- **Record Delete.** To remove individual profile records for privacy or hygiene reasons, see [Record Delete](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/ui/record-delete).

## Prerequisites {#prerequisites}

Before you begin, ensure that you have:

- Access to Adobe Experience Platform and the sandbox that contains the datasets you want to review.
- Permission to view the dataset catalog and, if you plan to set, change, or remove a retention policy, permission to modify dataset retention settings. See the [Access control overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home) for how Adobe Experience Platform permissions and roles work.
- The Adobe CXO plugin installed in CX Coworker.

For instructions on installing plugins, see the [Coworker UI guide](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide).

## Use the Data Management Agent {#use-the-data-management-agent}

Interact with the Data Management Agent through CX Coworker using natural language. Describe your goal as clearly as possible, then refine the results with follow-up questions.

>[!NOTE]
>
>Make sure you're working in the sandbox that contains the datasets you want to review before you begin.

To use the Data Management Agent:

1. Navigate to **[!UICONTROL CX Coworker]**. For access details, see the [Coworker UI guide](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide).
1. Enter a request. For example:

   *"Show me my largest event datasets."*

1. Review the results.
1. After reviewing a dataset, ask a follow-up question about it. For example:

   *"How actively is my Web Events dataset being used?"*

1. To set, change, or remove a retention policy, review the impact preview that the Data Management Agent returns, then confirm the request before it's applied.

## Supported use cases {#supported-use-cases}

Use these skills together as a workflow: start broad by finding your largest datasets, narrow down by checking how actively a dataset is used and modeling the impact of a candidate retention period, then set, change, or remove a retention policy once you're ready to act.

### Find your largest datasets {#find-your-largest-datasets}

To decide where to start a retention review, identify your largest Experience Event datasets and the ones most likely to need attention. Use the List datasets skill to surface these datasets by storage size, row count, existing retention status, and profile enablement, then filter by broad criteria such as dataset size, row count, or recent access to narrow the list. This skill is read-only. Coworker returns the results as a table you can scan and compare, along with visualizations that help you see which datasets stand out by size, row count, or data age. Once you've narrowed the list, use the Analyze dataset usage skill for a deeper look at how actively any one dataset is used.

Not every unused or abandoned dataset surfaced by this skill is a candidate for Experience Event TTL. See [Scope](#scope) for related tools that may be a better fit. Before setting a retention policy, confirm that the dataset is an Experience Event dataset.

For example:

- "Show me my largest event datasets."
- "Show me datasets larger than 100 GB that don't have data lake retention set."
- "I need to remove about 2 TBs of data. Where should I start?"
- "Can you help me find data that's orphaned, abandoned, or unused?"
- "Prioritize datasets with no access in the last 90 days."

### Check how actively a dataset is used {#check-how-actively-a-dataset-is-used}

Before you decide whether a dataset is a good candidate for a retention policy, find out how actively it's being used. Use the Analyze dataset usage skill to evaluate a specific dataset across nine deterministic signals — for example, recent ingestion activity, query activity, schema stability, and whether the dataset feeds other Adobe Experience Platform applications. This skill is read-only. Coworker returns the resulting usage tier along with a breakdown of the underlying signals and a plain-language summary of what they indicate about the dataset.

<!-- TODO(author): Confirm final usage-tier names and thresholds with engineering before publishing. Both the tier labels and the day-based thresholds behind them were still under discussion as of the kickoff meeting. See execution-brief.md, U2 and U3. -->

For example:

- "How actively is my Web Events dataset being used?"

### Deep dive into a dataset's retention posture {#deep-dive-into-a-datasets-retention-posture}

Before you commit to a specific retention period, find out what it would actually keep or remove. Use the Analyze dataset retention skill to review a dataset's storage metrics and the age distribution of the data it contains, and to model, as an approximation based on that age distribution, how much data a candidate retention period would keep or remove — by row count and storage size. This skill is read-only. Coworker returns this data-age and impact analysis directly in the conversation, so you can compare it against the dataset's current retention status before deciding whether to change it.

For example:

- "What would be the impact if I set a 60-day retention period on this dataset?"

### Set, change, or remove a retention policy {#set-change-or-remove-a-retention-policy}

Once you've decided on a retention period, apply it with the Manage dataset retention skill, which sets, changes, or removes a data-lake retention (TTL) policy on a dataset. Unlike Analyze dataset retention, which lets you explore potential impact without committing to anything, this skill's preview is the final check before a real change is made: describing the change you want doesn't apply it. The skill shows you the proposed impact first, and only changes the policy after you explicitly approve the request.

>[!IMPORTANT]
>
>The minimum data-lake retention period is 30 days; shorter periods aren't supported.

After you confirm a retention policy, the Adobe Experience Platform UI may take a short time to reflect the change. Removal of expired data is a separate process: data older than the retention period isn't purged instantly, but during a scheduled purge run. See the [Experience Event dataset retention (TTL) guide](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/experience-event-dataset-retention-ttl-guide) for more on how retention and purging work.

<!-- TODO(author): The kickoff demo described the purge as completing within about 24 hours of confirmation, but the Experience Event dataset retention (TTL) guide linked above states TTLs are evaluated and processed every 30 days. These sources conflict on the production purge cadence — confirm the actual cadence with the PM/engineering owner before this document states a specific timeframe. -->

Every retention change — setting, changing, or removing a policy — is recorded in an audit trail that includes who made the change, when, and what changed. You can review this directly in the Adobe Experience Platform audit log, with a link back to the relevant Adobe Experience Platform screen where available.

<!-- TODO(author): No authoritative Experience League page could be verified specifically for an Adobe Experience Platform "audit log" (candidate URLs returned 404, and the Catalog Service overview page doesn't reference one). Confirm with the PM/engineering owner exactly where customers should review retention audit events, and whether Coworker always surfaces a direct link to the relevant AEP screen or only in some cases. -->

For example:

- "Set the retention on this dataset to 60 days."
- "Remove the retention policy on this dataset."

## How the Data Management Agent works {#how-the-data-management-agent-works}

You can trust that the same inputs will always produce the same usage tier: the Analyze dataset usage skill calculates usage classifications using deterministic formulas rather than AI-generated estimates. Retention-impact modeling is also calculated programmatically rather than through AI-generated estimates, though it remains an approximation rather than an exact measurement. The information you see always reflects the current state of your sandbox, because the skills read data directly from Adobe Experience Platform services rather than a delayed or cached copy.

## Best practices {#best-practices}

Keep the following practices in mind when using the Data Management Agent:

- **Start with discovery.** Use the List datasets skill to review your largest datasets, and any that appear unused or abandoned, before you deep-dive into any single dataset.
- **Review the impact preview before you confirm.** Review what would be kept and removed before you approve the request.
- **Allow time for the change to appear.** After you confirm a retention change in CX Coworker, allow a short time for the Adobe Experience Platform UI to reflect it.

## Limitations {#limitations}

The Data Management Agent recommends retention candidates — it doesn't decide or apply a retention policy without your explicit confirmation.

<!-- TODO(author): Confirm that all four skills are generally available at publication time. As of the kickoff meeting, migration to production was still in progress and one skill depended on an MCP server pending an ARB review. See execution-brief.md, U4. -->

## Next steps {#next-steps}

After reading this guide, you should understand how to use the Data Management Agent in CX Coworker to find, analyze, and manage data-lake retention on your Experience Event datasets.

For more information, see the [Experience Event dataset retention (TTL) guide](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/experience-event-dataset-retention-ttl-guide).
