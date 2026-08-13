---
description: Browse Coworker Chat use cases and sample prompts, organized by area across data insights, audiences, journeys, and platform operations.
title: Coworker Chat Use Cases
---
# Coworker Chat use cases{#use-cases}

Coworker Chat lets you query, analyze, and act on your [!DNL Experience Platform] data using natural language instead of navigating multiple UIs or writing queries by hand. This page catalogs the use cases practitioners rely on most, organized by work area: data insights, audiences, journeys, foundational elements, and sandbox tooling. Each entry includes the skill it invokes, the applications it works with, and sample prompts you can copy, adapt to your own data, and refine through conversation.

## Data insights

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Pull CJA reports & metrics](data-insights/analytics-chat.md) | Query CJA in real time to pull metrics, dimensions, segments, and data views | `cja` | Customer Journey Analytics (CJA) | "Show me page views for the last 30 days" · "List top segments in the master data view" |
| Comparative analysis | Compare metrics across channels, time periods, or segments side by side | `cja` | Customer Journey Analytics (CJA) | "Compare revenue by channel month over month" · "How does mobile vs desktop conversion look this quarter?" |
| Funnel analysis | Walk through multi-step conversion funnels with drop-off at each stage | `cja` | Customer Journey Analytics (CJA) | "Walk me through the checkout funnel" · "Show conversion funnel from PDP to purchase" |
| Forecasting | Project future metric values based on historical CJA data | `cja` | Customer Journey Analytics (CJA) | "Forecast sessions for the next 30 days" · "Are we on track to hit our revenue goal?" |
| [Root cause analysis](data-insights/root-cause-analysis.md) | Investigate why a metric changed: diagnose drops, spikes, and anomalies | `cja-root-cause-analysis` | Customer Journey Analytics (CJA) | "Why did conversions drop last week?" · "What caused the revenue spike on Jan 15?" |
| Executive summaries & KPI digests | Produce stakeholder-ready performance summaries, prescriptive recommendations, and slide deck outlines | `cja-executive-summary` | Customer Journey Analytics (CJA) | "Give me an executive summary of last month" · "Create a slide deck outline from this quarter's data" |
| [AA ↔ CJA data validation](data-insights/data-validation-aa-cja.md) | Compare, audit, and reconcile data between Adobe Analytics and Customer Journey Analytics | `aa-cja-validation` | Adobe Analytics + CJA | "Compare my AA report suite to my CJA data view" · "Validate page views between AA and CJA" |
| Operational time-series & causal analysis | Query and analyze historical time-series data for audiences, datasets, and journeys with causal attribution | `operational-stats-causal-analysis` | All Eligible Applications | "Show me audience size trends over the last 90 days" · "Why did my dataset row count spike on March 3?" |
| Create custom CJA skills | Turn analytical patterns into reusable, repeatable skills that persist across sessions | `cja-skill-creator` | Customer Journey Analytics (CJA) | "Turn this weekly revenue analysis into a reusable skill" · "Save this as a skill for monthly funnel reporting" |

## Audiences

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Create audiences from natural language](audiences/create-audience-from-natural-language.md) | Orchestrate step-by-step audience creation with user approval at each phase | `audience-creation-flow` | Real-Time CDP (RTCDP) | "Create an audience of users who purchased in the last 30 days" · "Build a segment for high-value loyalty members in California" |
| Build PQL definitions | Assemble audience definitions from XDM properties, behavioral events, or existing audiences; support aggregation and time windows | `segment-definition-assembly` | Real-Time CDP (RTCDP) | "Create a PQL for people who viewed 3+ products but didn't purchase" · "Add a 7-day time window to my event condition" |
| Search & find audiences | Find audiences by ID, name, semantic search; detect duplicates and analyze overlap | `audience-search` | Real-Time CDP (RTCDP) | "Find all loyalty audiences" · "Is there a duplicate of my 'Holiday Shoppers' segment?" |
| Estimate audience size | Estimate profile reach for a PQL expression using Adobe Experience Platform Preview API with polling | `audience-size-estimate` | Real-Time CDP (RTCDP) | "How large is this audience?" · "Estimate reach for this PQL expression" |
| Audience size waterfall | Decompose a PQL into sub-predicates and show how each condition contributes to final audience size | `audience-size-waterfall` | Real-Time CDP (RTCDP) | "Show me the waterfall for this PQL" · "Break down how each condition reduces the audience" |
| Discover XDM fields for targeting | Search fields by name, description, or data value; see where they live and where they're already used | `field-discovery` | Real-Time CDP (RTCDP) | "Which fields can I use to target loyalty customers?" · "Find fields related to purchase history" |
| Publish / save audiences | Persist audience definitions to Experience Platform Segmentation Service with naming conventions and compliance checks | `audience-publish` | Real-Time CDP (RTCDP) | "Save this as a draft" · "Publish the audience with name 'Spring Sale Buyers'" |

## Journeys

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Create journeys from natural language](journeys/create-journey-from-natural-language.md) | Orchestrate journey creation in AJO from a text prompt or an uploaded image/flowchart | `journey-create` | Adobe Journey Optimizer (AJO) | "Create a welcome journey that sends an email after signup, waits 3 days, then sends a follow-up" · "Build a journey from this uploaded flowchart image" |
| Analyze journey conflicts | Detect audience overlap, schedule collisions, and deduplication issues between active journeys | `journey-analyze-conflict` | Adobe Journey Optimizer (AJO) | "Does my cart abandonment journey conflict with any other journeys?" · "Check for audience overlap between my active journeys" |
| Analyze journey fallout | Identify where and why customers drop off during a journey, and detect patterns in behavior leading to disengagement | `journey-analyze-fallout` | Adobe Journey Optimizer (AJO) | "Where are people dropping off in my Re-engagement journey?" · "Which nodes in journey X have the highest fallout?" |
| Analyze custom action errors | Identify when custom actions are failing or error rates spike within a journey, and diagnose root causes before failures cascade into broader disruption | `journey-analyze-custom-action` | Adobe Journey Optimizer (AJO) | "Why are custom actions failing in my Loyalty Signup journey?" · "Show me the error rate for custom action ExternalPush in my Welcome journey." |
| [Create, edit, and manage loyalty challenges](journeys/create-loyalty-challenge.md) | Simplify and accelerate loyalty program management | `loyalty` | Adobe Journey Optimizer (AJO) | "Create a challenge encouraging members to try a new seasonal beverage" · "Show me loyalty challenges with the highest member drop-off rates." |

## Foundational elements

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Product knowledge & documentation | Answer how-to, conceptual, troubleshooting, and best-practice questions from official Adobe docs | `product-knowledge` | All Eligible Applications | "How do I set up a streaming destination?" · "What's the difference between batch and streaming segmentation?" |
| Query Experience Platform / Journey Optimizer entities | Serve as the primary entry point for questions about your platform entities; route to KG, field discovery, or APIs as needed | `operational-insights` | All Eligible Applications | "How many datasets do I have?" · "Show me all active journeys" · "List my destinations" |
| Knowledge Graph queries | Aggregate counts, cross-entity joins, relationship lookups, and metadata exploration via single SQL queries | `knowledge-graph` | All Eligible Applications | "Which audiences use this dataset?" · "Show me relationships between schemas and datasets" |
| Experience Platform / Journey Optimizer / Customer Journey Analytics API operations | Provide a direct API gateway for mutations, real-time state checks, and entity types not in the Knowledge Graph | `cxo-api` | All Eligible Applications | "Delete dataset X" · "Check the status of my batch ingestion job" |
| Entity resolution & linking | Use semantic and lexical search to resolve entity mentions to actual Experience Platform entities and discover XDM fields | `entity-linking` | Adobe Experience Platform | "Resolve 'Holiday Shoppers' to an actual audience" · "Find me fields related to purchase history" |
| Manage custom skills | Save, modify, or delete user-owned reusable skills that persist across sessions | `manage-skill` | All Eligible Applications | "Save that workflow as a skill" · "Delete my weekly report skill" · "Turn this into a reusable skill" |

## Sandbox tooling

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Move objects across sandboxes](/help/agents/sandbox-tooling.md) | Seamlessly migrate schemas, audiences, and other object configurations across sandboxes, with dependencies auto-resolved | `sandbox-tooling-workflow` | Adobe Experience Platform | "Move schema Luma Loyalty Members Platinum from current sandbox to prod sandbox" · "Promote the US Gold Loyalty Members audience to stage" |

## Experience Generation

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Update AEM pages | Perform actions such as updating, removing, replacing, or adding content elements to keep experiences accurate and current. Inputs can be natural language or visual annotations like PDFs or screenshots. | `aem-sites-pages-update` | AEM as a Cloud Service - Sites | On &lt;url&gt; update the headline to Hello World<br>on &lt;your-publish-URL&gt; change “Take our Coffee Quiz” button to a more engaging version<br>Update &lt;URL&gt; based on the attached<br>on https://author-p149891-e1546481.adobeaemcloud.com/content/frescopa/en/index.html i want to a add a new teaser section to the bottom of the page about a promotion we are running in the month of august that is buy a coffee machine and get 2 bags of coffee free. Also find image of friends drinking coffee and use that in the teaser |
| Update AEM in bulk | Perform bulk actions across multiple pages at the same time such as removing, replacing, or adding content elements to keep experiences accurate and current. | `aem-sites-pages-bulkreplace` | AEM as a Cloud Service - Sites | on &lt;aem path&gt; update all pages that contain copy "MyBarista" to "BrewPass" |
| Edit Content Fragments  | Use natural language to manage a single Content Fragment or hundreds at once. AI handles search, creation, updates, publishing, tagging, and other content operations while automatically enforcing the appropriate governance workflow. | `aem-sites-contentfragments-bulk-edit` | AEM as a Cloud Service - Sites | find Content Fragments under /content/dam/agentic-cf whose calories field is set to 150  and update 20 also update the 'Serving Style' field on the same fragments to 'Iced'<br>Create 3 fragments ones under /content/dam/agentic-cf  name them 'Cortado Freddo Summer’, 'Turkish Coffee Summer’, 'Café de Olla Summer’ and 'Calories' 150 each. Tag the 3 fragments with the 'Frescopa : Coffee' tag |
| Go from Figma to Visual Content Fragment - technical | Import designs directly from Figma into Adobe Experience Manager using natural language. The skill automatically creates the required content model, content fragment, assets, and visualization template, enabling business users to move from design to web-ready content in minutes without manual setup. | `aem-sites-visualcontentfragments-create` | AEM as a Cloud Service - Sites | Import from &lt;figma path&gt; |
| Read/write AEM form content | Optimize and manage Content Fragments for AI-powered experiences through readiness checks that include semantic analysis and impact assessment. Evaluates content quality, metadata, structure, schema compliance, and references to surface issues affecting search, publishing, translation, or headless delivery. Analyzes dependencies across Content Fragments, collections, assets, models, and pages to identify risks and recommend safe actions. Finally it provides assessments with guided, human-reviewed remediation steps. | `aem-forms-adaptiveform-author` | AEM as a Cloud Service - Forms | Create a new form based on attached brief &#47; screenshot<br>Now bring this form in line with attached guidelines - the standard wizard structure and approved wording<br>Create a coffee subscription form with personal info, subscription preferences. Keep only relevant fields mandatory, use wizard layout for easier navigation. |
