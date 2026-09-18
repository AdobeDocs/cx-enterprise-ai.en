---
description: Browse Coworker Chat use cases and sample prompts, organized by area across data insights, audiences, journeys, and platform operations.
title: Coworker Chat Use Cases
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: ''
---
# Coworker Chat use cases{#use-cases}

Coworker Chat lets you query, analyze, and act on your [!DNL Experience Platform] data using natural language instead of navigating multiple UIs or writing queries manually. This page catalogs the use cases practitioners rely on most, organized by work area: data insights, audiences, journeys, foundational elements, and sandbox tooling. Each entry includes the skill it invokes, the applications it works with, and sample prompts you can copy, adapt to your own data, and refine through conversation.

>[!NOTE]
>
>Coming soon: 
>
>New AEM agentic capabilities through CX Enterprise Coworker, built to help you do more, faster.
>
>All eligible customers will get access to Adobe Experience Manager agentic capabilities in Coworker, on a rolling basis.
>
>See also [AI in AEM - Overview of Agentic Capabilities in AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/overview).

## Brand Experience

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Update AEM pages  | Perform actions such as updating, removing, replacing, or adding content elements to keep experiences accurate and current. Inputs can be natural language or visual annotations like PDFs or screenshots. | `aem-sites-pages-update` | Adobe Experience Manager (AEM) - AEM Sites | On &lt;URL&gt; update the headline to Hello World<br><br>on &lt;URL&gt; change "Take our Coffee Quiz" button to a more engaging version<br><br>Update &lt;URL&gt; based on the attached<br><br>on &lt;URL&gt; I want to a add a new teaser section to the bottom of the page about a promotion we are running in the month of august that is buy a coffee machine and get 2 bags of coffee free. Also find image of friends drinking coffee and use that in the teaser |
| Update AEM in bulk | Perform bulk actions across multiple pages at the same time such as removing, replacing, or adding content elements to keep experiences accurate and current. | `aem-sites-pages-bulkreplace` | Adobe Experience Manager (AEM) - AEM Sites | on &lt;aem path&gt; update all pages that contain copy "MyBarista\" to "BrewPass" |
| Go from Figma to Visual Content Fragment | Import designs directly from Figma into Adobe Experience Manager using natural language. The skill automatically creates the required content model, content fragment, assets, and visualization template, enabling business users to move from design to web-ready content in minutes without manual setup. | `aem-sites-visualcontentfragments-create` | Adobe Experience Manager (AEM) - AEM Sites | Import from &lt;Figma_URL&gt; |

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Create form | Generate a new Adaptive Form from a plain-language description, an attached brief, an image, or a PDF | `aem-forms-adaptiveform-create` | Adobe Experience Manager (AEM)  - AEM Forms | "Create an employee onboarding form"<br><br>"Create a form using the attached brief (image or pdf)"<br><br>"Create a &lt;form type&gt; adaptive form" |
| Edit/Update form | Modify an existing form - add/edit fields, adjust simple layout, configure submit actions, or apply changes from an attached guidelines document | `aem-forms-adaptiveform-edit` | Adobe Experience Manager (AEM) - AEM Forms | "Add Middle Name field below First Name field"<br><br>"Put First Name and Last Name fields in a 2 column layout, 50/50"<br><br>"Configure the form to send data to a REST endpoint"<br><br>"Update this form to match the attached guidelines document"<br><br>"Add &lt;field name&gt; field below &lt;existing field&gt; field" |
| Add business logic | Create simple rules, such as showing or hiding a field based on another field's value | `aem-forms-adaptiveform-edit` | Adobe Experience Manager (AEM)  - AEM Forms | "Show the Company field only when Employee Type is Contractor"<br><br>"Show the &lt;field&gt; field only when &lt;other field&gt; is &lt;value&gt;" |
| Embed form | Place an existing or newly created form onto a designated AEM Sites page (supported on Edge Delivery Services pages only) | `aem-forms-adaptiveform-embed` | Adobe Experience Manager (AEM) - AEM Forms | "Embed this form on the homepage of our site"<br><br>"Embed this form on &lt;page path&gt;" |

**Related information**

* [Agentic Capabilities in AEM: Brand Experience - Experience Production - Sites](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-sites)

* [Agentic Capabilities in AEM: Brand Experience - Experience Production - Forms](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-forms)

### Development

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Manage Cloud Manager pipelines| Create, run, and monitor AEM Cloud Manager pipelines, including logs, artifacts, variables, and settings | `cloud-manager-pipeline-management` | Adobe Experience Manager (AEM)  | "List pipelines for program 12345"<br><br>"What is the status of my most recent pipeline?" |
| Manage Cloud Manager environments | Create, configure, and maintain AEM Cloud Manager environments, including RDEs, environment variables, logs, and backups | `cloud-manager-environment-management` | Adobe Experience Manager (AEM)  | "List my environments for program 12345"<br><br>"Reset my RDE" |
| Manage Cloud Manager programs | List, inspect, and delete AEM Cloud Manager programs, including their pipelines and environments | `cloud-manager-program-management` | Adobe Experience Manager (AEM)  | "List my Cloud Manager programs"<br><br>"Get details for program 12345" |
| Manage AEM release update schedules | Configure daily Quiet Hours and Update-Free Periods for automated maintenance, and view Adobe's global Code-Freeze windows | `cloud-manager-release-management` | Adobe Experience Manager (AEM)  | "What's my current Quiet Hours window?"<br><br>"Schedule an update-free period from Dec 20 to Jan 2" |

**Related information**

* [Agentic Capabilities in AEM: Brand Experience - Development](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/development/use-cases)

### Onboarding

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Guided end-to-end onboarding | Orchestrates the full onboarding lifecycle, repository selection, delegation to the folder, tag, metadata, import, and search sub-skills, if you do not know the specific onboarding task that you need. | `aem-onboarding-workflow` | Adobe Experience Manager (AEM) - AEM Assets | "Onboard our team to AEM Assets"<br><br>"Walk me through AEM DAM onboarding" |
| Design and create folder hierarchies | Recommends and creates scalable folder structures in AEM Assets (under `/content/dam`) based on business needs or CSV inputs. | `aem-folder-management` | Adobe Experience Manager (AEM) - AEM Assets | "Recommend a folder structure for our lifestyle marketing assets"<br><br>"Create folders based on this CSV file" |
| Design and create tags | Designs and creates controlled tag vocabularies under `/content/cq:tags` - namespaces, hierarchical tags, and batch tag operations. | `aem-tag-taxonomy` | Adobe Experience Manager (AEM) - AEM Assets | "Design a tag taxonomy with namespaces for our product categories"<br><br>"Import tags from this CSV"<br><br>"Create these hierarchical tags in AEM" |
| Create and assign metadata forms | Designs and creates custom metadata forms, the authoring UI content authors use, from a CSV, table, requirements doc, or description, then optionally assigns them to folders. | `aem-metadata-form` | Adobe Experience Manager (AEM) - AEM Assets | "Create a metadata form from this list of fields"<br><br>"Assign this form to the `campaigns` folder" |

**Related information**

* [Agentic Capabilities in AEM: Brand Experience - Onboarding](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/onboarding/use-cases)

## Content Advisor

### Content Discovery

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Search by semantic theme | Find assets by concept, mood, or visual theme using AI-powered semantic matching. | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | "Find me morning coffee lifestyle images" |
| Search by custom metadata | Filter assets by custom metadata fields (for example, Coffee Blend, Brand, Roast Level). | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | "Find assets where `Coffee Blend` is `Morning Muse`"<br><br>"Get me assets whose license is not expired"<br><br>"Find me assets whose Campaign Name is not set (the property must be indexed for appropriate results)." |
| Search by approval status | Filter assets based on the approval status. For example, approved, in-review, rejected, or missing status. | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | "Show me all approved assets in the `Campaign` folder" |
| Search by folder/path | Identify assets by interpreting natural language prompts that reference folder names in AEM. You can simply mention the folder in their prompt, without manually navigating through the repository, significantly reducing the number of clicks needed to locate the right content. | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | "Are there any svgs in folder `WKND`"?<br><br>"Show assets modified after Nov 1 2025 in folder `WKND`" |

**Related information**

* [Agentic Capabilities in AEM: Content Advisor - Content Discovery](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/discovery/use-cases)

### Content Optimization

| Use Case | Description | Skill(s) | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| High-resolution rendition creation and Channel-optimized renditions | Generate new renditions of an asset at a specified resolution and quality level, making it easy to prepare channel-ready variations without manual editing. You can also produce renditions tailored to platform-specific requirements, such as Instagram Stories, ensuring assets meet format, ratio, and quality guidelines automatically. | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | "Create a `2000px` rendition as `JPEG` with `80% quality`"<br><br>"Create a rendition for an Instagram story" |
| Branded overlays and composite generation | Apply promotional graphics, overlays, or badges to existing assets with precise placement, supporting rapid creation of campaign-ready composites. | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | "Overlay the image with `30%` discount graphics over the promotional banner, placing it `100px` from the center" |
| Image enhancements, background color adjustments, orientation transformations | Apply visual improvements (sharpening image), replace background colors, and perform orientation transformations. | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | "Change background color of the `PNG` to `#ff8932`"<br><br>"Sharpen the image"<br><br>"Mirror the image horizontally" |

**Related information**

* [Agentic Capabilities in AEM: Content Advisor - Content Optimization](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/content-optimization/use-cases)

## Brand Governance

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Guideline & segment lookup | Retrieve detailed brand guidelines, scoped by segment, market, or category | enterprise-context | Adobe Experience Manager (AEM)  | "What are the tone-of-voice guidelines for this brand?"<br>"List the claim categories used in the health vertical" |
| Evaluate content against brand guidelines | Evaluate a published/authored page, text block, or image against configured brand checks | aem-governance | Adobe Experience Manager (AEM)  | "Evaluate this landing page against SecurBank guidelines"<br>"Does this tagline pass our tone-of-voice checks?" |
| Debug AEM permissions | Debug / understand permission policies, ACLs, and inheritance rules. | aem-governance | Adobe Experience Manager (AEM)  | "Why can principal admin write `/content/folder/us` on `https://author/` ?"<br>"Why can't sample-author write in `/content/dam` on `https://author`" |

**Related information**

* [Agentic Capabilities in AEM: Brand Governance](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-governance/use-cases)

## Data insights

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Pull CJA reports & metrics](data-insights/analytics-chat.md) | Query CJA in real time to pull metrics, dimensions, segments, and data views | `cja` | Customer Journey Analytics (CJA) | "Show me page views for the last 30 days" <br> "List top segments in the master data view" |
| Comparative analysis | Compare metrics across channels, time periods, or segments side by side | `cja-root-cause-analysis`, `cja`, `dx-api`, `knowledge-graph` | Customer Journey Analytics (CJA) | "Compare revenue by channel month over month" <br> "How does mobile vs desktop conversion look this quarter?" |
| Campaign performance | Measure how campaigns, channels, and web properties performed over a given period. | `cja`, `dx-api`, `knowledge-graph` | | "How did our Acrobat web campaigns perform last month?" |
| Funnel analysis | Walk through multi-step conversion funnels with drop-off at each stage | `cja` | Customer Journey Analytics (CJA) | "Walk me through the checkout funnel" <br> "Show conversion funnel from PDP to purchase" |
| Forecasting | Project future metric values based on historical CJA data | `cja` | Customer Journey Analytics (CJA) | "Forecast sessions for the next 30 days" <br> "Are we on track to hit our revenue goal?" |
| [Root cause analysis](data-insights/root-cause-analysis.md) | Investigate why a metric changed: diagnose drops, spikes, and anomalies | `cja-root-cause-analysis` | Customer Journey Analytics (CJA) | "Why did conversions drop last week?" <br> "What caused the revenue spike on Jan 15?" |
| Executive summaries & KPI digests | Produce stakeholder-ready performance summaries, prescriptive recommendations, and slide deck outlines | `cja-executive-summary`, `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, `cja-reporting`, `cja`, `dx-api` | Customer Journey Analytics (CJA) | "Give me an executive summary of last month" <br> "Create a slide deck outline from this quarter's data" |
| [AA ↔ CJA data validation](data-insights/data-validation-aa-cja.md) | Compare, audit, and reconcile data between Adobe Analytics and Customer Journey Analytics, especially when upgrading from Adobe Analytics to Customer Journey Analytics | `aa-cja-validation`, `cja`, `dx-api` | Adobe Analytics + CJA | "Compare my AA report suite to my CJA data view" <br> "Validate page views between AA and CJA" |
| Operational time-series & causal analysis | Query and analyze historical time-series data for audiences, datasets, and journeys with causal attribution | `operational-stats-causal-analysis` | All Eligible Applications | "Show me audience size trends over the last 90 days" <br> "Why did my dataset row count spike on March 3?" |
| Create custom CJA skills | Turn analytical patterns into reusable, repeatable skills that persist across sessions | `cja-skill-creator` | Customer Journey Analytics (CJA) | "Turn this weekly revenue analysis into a reusable skill" <br> "Save this as a skill for monthly funnel reporting" |

## Audiences

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Create audiences from natural language](audiences/create-audience-from-natural-language.md) | Orchestrate step-by-step audience creation with user approval at each phase | `audience-creation-flow` | Real-Time CDP (RTCDP) | "Create an audience of users who purchased in the last 30 days" <br> "Build a segment for high-value loyalty members in California" |
| Build PQL definitions | Assemble audience definitions from XDM properties, behavioral events, or existing audiences; support aggregation and time windows | `segment-definition-assembly` | Real-Time CDP (RTCDP) | "Create a PQL for people who viewed 3+ products but didn't purchase" <br> "Add a 7-day time window to my event condition" |
| Search & find audiences | Find audiences by ID, name, semantic search; detect duplicates and analyze overlap | `audience-search` | Real-Time CDP (RTCDP) | "Find all loyalty audiences" <br> "Is there a duplicate of my 'Holiday Shoppers' segment?" |
| Estimate audience size | Estimate profile reach for a PQL expression using Adobe Experience Platform Preview API with polling | `audience-size-estimate` | Real-Time CDP (RTCDP) | "How large is this audience?" <br> "Estimate reach for this PQL expression" |
| Audience size waterfall | Decompose a PQL into sub-predicates and show how each condition contributes to final audience size | `audience-size-waterfall` | Real-Time CDP (RTCDP) | "Show me the waterfall for this PQL" <br> "Break down how each condition reduces the audience" |
| Discover XDM fields for targeting | Search fields by name, description, or data value; see where they live and where they're already used | `field-discovery` | Real-Time CDP (RTCDP) | "Which fields can I use to target loyalty customers?" <br> "Find fields related to purchase history" |
| Publish / save audiences | Persist audience definitions to Experience Platform Segmentation Service with naming conventions and compliance checks | `audience-publish` | Real-Time CDP (RTCDP) | "Save this as a draft" <br> "Publish the audience with name 'Spring Sale Buyers'" |

## Journeys

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Create journeys from natural language](journeys/create-journey-from-natural-language.md) | Orchestrate journey creation in AJO from a text prompt or an uploaded image/flowchart | `journey-create` | Adobe Journey Optimizer (AJO) | "Create a welcome journey that sends an email after signup, waits 3 days, then sends a follow-up" <br> "Build a journey from this uploaded flowchart image" |
| Analyze journey conflicts | Detect audience overlap, schedule collisions, and deduplication issues between active journeys | `journey-analyze-conflict` | Adobe Journey Optimizer (AJO) | "Does my cart abandonment journey conflict with any other journeys?" <br> "Check for audience overlap between my active journeys" |
| Analyze journey fallout | Identify where and why customers drop off during a journey, and detect patterns in behavior leading to disengagement | `journey-analyze-fallout` | Adobe Journey Optimizer (AJO) | "Where are people dropping off in my Re-engagement journey?" <br> "Which nodes in journey X have the highest fallout?" |
| Analyze custom action errors | Identify when custom actions are failing or error rates spike within a journey, and diagnose root causes before failures cascade into broader disruption | `journey-analyze-custom-action` | Adobe Journey Optimizer (AJO) | "Why are custom actions failing in my Loyalty Signup journey?" <br> "Show me the error rate for custom action ExternalPush in my Welcome journey." |
| [Create, edit, and manage loyalty challenges](journeys/create-loyalty-challenge.md) | Simplify and accelerate loyalty program management | `loyalty` | Adobe Journey Optimizer (AJO) | "Create a challenge encouraging members to try a new seasonal beverage" <br> "Show me loyalty challenges with the highest member drop-off rates." |

## Foundational elements

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Product knowledge & documentation | Answer how-to, conceptual, troubleshooting, and best-practice questions from official Adobe docs | `product-knowledge` | All Eligible Applications | "How do I set up a streaming destination?" <br> "What's the difference between batch and streaming segmentation?" |
| Query Experience Platform / Journey Optimizer entities | Serve as the primary entry point for questions about your platform entities; route to KG, field discovery, or APIs as needed | `operational-insights` | All Eligible Applications | "How many datasets do I have?" <br> "Show me all active journeys" <br> "List my destinations" |
| Knowledge Graph queries | Aggregate counts, cross-entity joins, relationship lookups, and metadata exploration via single SQL queries | `knowledge-graph` | All Eligible Applications | "Which audiences use this dataset?" <br> "Show me relationships between schemas and datasets" |
| Experience Platform / Journey Optimizer / Customer Journey Analytics API operations | Provide a direct API gateway for mutations, real-time state checks, and entity types not in the Knowledge Graph | `cxo-api` | All Eligible Applications | "Delete dataset X" <br> "Check the status of my batch ingestion job" |
| Entity resolution & linking | Use semantic and lexical search to resolve entity mentions to actual Experience Platform entities and discover XDM fields | `entity-linking` | Adobe Experience Platform | "Resolve 'Holiday Shoppers' to an actual audience" <br> "Find me fields related to purchase history" |
| Manage custom skills | Save, modify, or delete user-owned reusable skills that persist across sessions | `manage-skill` | All Eligible Applications | "Save that workflow as a skill" <br> "Delete my weekly report skill" <br> "Turn this into a reusable skill" |
| Monitor streaming capacity & breaches | Check current and historical streaming usage, capacity, and breach status across sandboxes | `observability-streaming-capacity`, `observability-streaming-usage`, `observability-capacity-breaches` | Adobe Experience Platform | "What is my current streaming capacity in my current sandbox?" <br> "Is my current sandbox breaching capacity limits in the last week?" |
| [View health check assessment results](https://experienceleague.adobe.com/en/docs/experience-platform/run-and-operate/health-checks/overview) | View the latest health check assessment for your sandbox, drill into a failing check, and see the affected entities | `rao-view-latest-health-checks-assessment` | Adobe Experience Platform | "What's wrong in my sandbox?" <br> "Tell me about my latest health check assessment" <br> "What are the issues for the custom namespace description check?" |
| Remediate health check issues | Fix flagged identity namespace, merge policy, and schema issues directly from chat, with your approval before any change is made | `rao-remediate-identity-namespace-description`, `rao-remediate-merge-policy-duplicate-name`, `rao-remediate-missing-audit-field-group`, `rao-remediate-default-merge-policy-naming` | Adobe Experience Platform | "Fix identity namespace descriptions" <br> "Fix duplicate merge policy names" <br> "Fix schemas missing the audit field group" <br> "Fix default merge policy naming" |

## Data Management

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Find data worth optimizing or cleaning up](./data-management/manage-data-lake-retention.md) | Get a sense of whether your Experience Event data can be optimized by surfacing your largest, least-used, or forgotten datasets as candidates for cleanup or a data lake retention policy | List datasets | Adobe Experience Platform | "I have a feeling my data can be optimized" <br> "Help me understand the value of my data" <br> "Optimize my sandbox data" <br> "Clean up my sandbox datasets" |
| [Investigate usage and manage retention for a dataset](./data-management/manage-data-lake-retention.md) | Once you've found a dataset worth a closer look, find out how actively it's used, model the impact of a potential data lake retention policy, and set, change, or remove that policy when you're ready, with your review and approval before anything changes | Analyze dataset usage, Analyze dataset retention, Manage dataset retention | Adobe Experience Platform | "How actively is my Web Events dataset being used?" <br> "What would be the impact if I set a 60-day retention period on this dataset?" |

## Sandbox tooling

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Move objects across sandboxes](/help/agents/sandbox-tooling.md) | Seamlessly migrate schemas, audiences, and other object configurations across sandboxes, with dependencies auto-resolved | `sandbox-tooling-workflow` | Adobe Experience Platform | "Move schema Luma Loyalty Members Platinum from current sandbox to prod sandbox" <br> "Promote the US Gold Loyalty Members audience to stage" |

## Customer alerts

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Manage alert subscriptions | View and manage alert subscriptions through natural-language conversations. | `alerts-subscribe` | Adobe Experience Platform | "What alerts am I subscribed to?"<br><br>"Subscribe me to this alert."<br><br>"Remove my subscription to this alert." |
| Review alert activity | Review current alert status and historical alert activity for a specified time period. | `alerts-list` | Adobe Experience Platform | "What happened in the last 24 hours?"<br><br>"What alerts were triggered in the last 24 hours?"<br><br>"Show active alerts from the last seven days." |
| Identify recurring alert patterns | Analyze alert history to identify frequently triggered alert types and operational trends. | `alerts-list` | Adobe Experience Platform | "Show me the top 3 triggered alert types."<br><br>"Which alert types occurred most frequently this month?"<br><br>"What alert patterns do you see in the last seven days?" |
| Focus on high-priority issues | Filter alert activity by severity to prioritize investigation efforts. | `alerts-list` | Adobe Experience Platform | "Only show high-severity alerts."<br><br>"What critical alerts were triggered this week?"<br><br>"Show critical alerts from the last 30 days." |
| Understand the impact radius of alerts | Identify the objects most affected by alerts and determine where investigation should begin. | `alerts-list` | Adobe Experience Platform | "What are the top 5 impacted objects?"<br><br>"Which objects are associated with the most high-severity alerts?" |
| Connect alert types to impacted objects | Analyze relationships between alert types and affected resources. | `alerts-list` | Adobe Experience Platform | "Which alert types impacted this dataset most often?"<br><br>"Show the relationship between alert types and impacted objects."<br><br>"Which alert type affected the top impacted object most frequently?" |
| Focus on My Alerts | Analyze alerts that you subscribe to and are responsible for monitoring. | `alerts-list` | Adobe Experience Platform | "Show me the high-severity alerts I subscribe to."<br><br>"What alerts from My Alerts were triggered this week?"<br><br>"Do any of my subscribed alerts require attention?" |

## Workflow and planning

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Manage Planning workspace | Build and evolve Workfront Planning workspaces, sections, record types, and fields to organize programs and track work | `manage-workfront-planning`, `wf-planning-solution-architect` | Workfront Planning | "Create a workspace called MKG Hub and set up record types to track programs by region" <br> "Set up the record types and relationships needed to track MKG programs across channels and region" |
| Manage Planning records | Create and update planning records (campaigns, briefs) and their field values within a workspace | `manage-workfront-planning` | Workfront Planning | "Create a brief for the Fall Brand Launch campaign with the objective, target audience, and key messages" <br> "Update the Fall Brand Launch brief with the budget and primary channels" |
| Create and manage projects | Spin up and structure projects - apply templates, set priorities and budgets, sequence tasks, add phases and dependencies, and assign people or roles | `manage-workfront-workflow` | Workfront Workflow | "Create a Spring campaign, set it high-priority with a $200K budget, and sequence the tasks" <br> "Create a Workfront project plan named [project name] from [project template]" <br> "Build a project plan for Fall Launch - Social Campaign with tasks for concepting, design, copy, and review" <br> "Add a new Email Marketing task and assign it to Rachel Smith" |
| Accelerate reviews & approvals | Set up multi-stage approvals, apply approval templates, add/remove approvers, send reminders, and make bulk updates | `manage-workfront-workflow` | Workfront Workflow | "Create a multi-stage approval - copy, design, legal - and remind anyone who hasn't approved" <br> "Remove Chris Smith from all open approvals and replace with Jane Francis" |
| Update task & work status | Mark tasks complete, update percent complete, and close out your work | `manage-workfront-workflow` | Workfront Workflow | "Mark my 'Produce key art' task on Fall Launch as complete" <br> "Close out my Fall Launch copy task at 100%" |
| Surface work insights | Ask exploratory questions to find at-risk work, unassigned tasks, open issues, and status across projects | `query-workfront` | Workfront Workflow | "Find incomplete tasks on current projects that aren't assigned to anyone and due this week" <br> "How many open issues are there across current projects?" |
| Summary of projects & tasks | Pull lists, tables, and counts of projects, tasks, issues, and assignments | `query-workfront` | Workfront Workflow | "Show me a table of my tasks that are ready to start, with the project name, task due date, and assigned user" <br> "Get me all tasks assigned to [user name]" |
| Track approvals & portfolio status | Check the status of your approvals and roll up incomplete work by portfolio | `query-workfront` | Workfront Workflow | "Show me the status of my approvals" <br> "Show me a table with incomplete issues that are part of the [Portfolio name] portfolio" |
