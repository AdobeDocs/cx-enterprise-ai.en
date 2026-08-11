---
description: Browse Coworker Chat use cases and sample prompts, organized by area across data insights, audiences, journeys, and platform operations.
title: Coworker Chat Use Cases
---
# Coworker Chat use cases{#use-cases}

Coworker Chat lets you query, analyze, and act on your [!DNL Experience Platform] data using natural language instead of navigating multiple UIs or writing queries by hand. This page catalogs the use cases practitioners rely on most, organized by work area: data insights, audiences, journeys, foundational elements, and sandbox tooling. Each entry includes the skill it invokes, the applications it works with, and sample prompts you can copy, adapt to your own data, and refine through conversation.

## Data insights

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Pull CJA reports & metrics](data-insights/analytics-chat.md) | Query CJA in real time to pull metrics, dimensions, segments, and data views | `cja` | Customer Journey Analytics (CJA) | "Show me page views for the last 30 days" · "List top segments in the master data view" |
| Comparative analysis | Compare metrics across channels, time periods, or segments side by side | `cja-root-cause-analysis`, `cja`, `dx-api`, `knowledge-graph` | Customer Journey Analytics (CJA) | "Compare revenue by channel month over month" · "How does mobile vs desktop conversion look this quarter?" |
| Campaign performance | Measure how campaigns, channels, and web properties performed over a given period. | `cja`, `dx-api`, `knowledge-graph` | | "How did our Acrobat web campaigns perform last month?" |
| Funnel analysis | Walk through multi-step conversion funnels with drop-off at each stage | `cja` | Customer Journey Analytics (CJA) | "Walk me through the checkout funnel" · "Show conversion funnel from PDP to purchase" |
| Forecasting | Project future metric values based on historical CJA data | `cja` | Customer Journey Analytics (CJA) | "Forecast sessions for the next 30 days" · "Are we on track to hit our revenue goal?" |
| [Root cause analysis](data-insights/root-cause-analysis.md) | Investigate why a metric changed: diagnose drops, spikes, and anomalies | `cja-root-cause-analysis` | Customer Journey Analytics (CJA) | "Why did conversions drop last week?" · "What caused the revenue spike on Jan 15?" |
| Executive summaries & KPI digests | Produce stakeholder-ready performance summaries, prescriptive recommendations, and slide deck outlines | `cja-executive-summary`, `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, `cja-reporting`, `cja`, `dx-api` | Customer Journey Analytics (CJA) | "Give me an executive summary of last month" · "Create a slide deck outline from this quarter's data" |
| [AA ↔ CJA data validation](data-insights/data-validation-aa-cja.md) | Compare, audit, and reconcile data between Adobe Analytics and Customer Journey Analytics, especially when upgrading from Adobe Analytics to Customer Journey Analytics | `aa-cja-validation`, `cja`, `dx-api` | Adobe Analytics + CJA | "Compare my AA report suite to my CJA data view" · "Validate page views between AA and CJA" |
| Operational time-series & causal analysis | Query and analyze historical time-series data for audiences, datasets, and journeys with causal attribution | `operational-stats-causal-analysis` | All Eligible Applications | "Show me audience size trends over the last 90 days" · "Why did my dataset row count spike on March 3?" |
| Create custom CJA skills | Turn analytical patterns into reusable, repeatable skills that persist across sessions | `cja-skill-creator` | Customer Journey Analytics (CJA) | "Turn this weekly revenue analysis into a reusable skill" · "Save this as a skill for monthly funnel reporting" |

## Audiences

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Create audiences from natural language](audiences/create-audience-from-natural-language.md) | Orchestrate step-by-step audience creation with user approval at each phase | `audience-creation-flow` | Real-Time CDP (RTCDP) | "Create an audience of users who purchased in the last 30 days" · "Build a segment for high-value loyalty members in California" |
| Build PQL definitions | Assemble audience definitions from XDM properties, behavioral events, or existing audiences; support aggregation and time windows | `segment-definition-assembly` | Real-Time CDP (RTCDP) | "Create a PQL for people who viewed 3+ products but didn't purchase" · "Add a 7-day time window to my event condition" |
| Search & find audiences | Find audiences by ID, name, semantic search; detect duplicates and analyze overlap | `audience-search` | Real-Time CDP (RTCDP) | "Find all loyalty audiences" · "Is there a duplicate of my 'Holiday Shoppers' segment?" |
| Estimate audience size | Estimate profile reach for a PQL expression using Adobe Experience Platform Preview API with polling | `audience-size-estimate` | Real-Time CDP (RTCDP) | "How large is this audience?" · "Estimate reach for this PQL expression" |
| Audience size waterfall | Decompose a PQL into sub-predicates and show how each condition contributes to final audience size | `audience-size-waterfall` | Real-Time CDP (RTCDP) | "Show me the waterfall for this PQL" · "Break down how each condition reduces the audience" |
| Discover XDM fields for targeting | Search fields by name, description, or data value; see where they live and where they're already used | `field-discovery` | Real-Time CDP (RTCDP) | "Which fields can I use to target loyalty customers?" · "Find fields related to purchase history" |
| Publish / save audiences | Persist audience definitions to Experience Platform Segmentation Service with naming conventions and compliance checks | `audience-publish` | Real-Time CDP (RTCDP) | "Save this as a draft" · "Publish the audience with name 'Spring Sale Buyers'" |

## Journeys

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Create journeys from natural language](journeys/create-journey-from-natural-language.md) | Orchestrate journey creation in AJO from a text prompt or an uploaded image/flowchart | `journey-create` | Adobe Journey Optimizer (AJO) | "Create a welcome journey that sends an email after signup, waits 3 days, then sends a follow-up" · "Build a journey from this uploaded flowchart image" |
| Analyze journey conflicts | Detect audience overlap, schedule collisions, and deduplication issues between active journeys | `journey-analyze-conflict` | Adobe Journey Optimizer (AJO) | "Does my cart abandonment journey conflict with any other journeys?" · "Check for audience overlap between my active journeys" |
| Analyze journey fallout | Identify where and why customers drop off during a journey, and detect patterns in behavior leading to disengagement | `journey-analyze-fallout` | Adobe Journey Optimizer (AJO) | "Where are people dropping off in my Re-engagement journey?" · "Which nodes in journey X have the highest fallout?" |
| Analyze custom action errors | Identify when custom actions are failing or error rates spike within a journey, and diagnose root causes before failures cascade into broader disruption | `journey-analyze-custom-action` | Adobe Journey Optimizer (AJO) | "Why are custom actions failing in my Loyalty Signup journey?" · "Show me the error rate for custom action ExternalPush in my Welcome journey." |

## Foundational elements

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| Product knowledge & documentation | Answer how-to, conceptual, troubleshooting, and best-practice questions from official Adobe docs | `product-knowledge` | All Eligible Applications | "How do I set up a streaming destination?" · "What's the difference between batch and streaming segmentation?" |
| Query Experience Platform / Journey Optimizer entities | Serve as the primary entry point for questions about your platform entities; route to KG, field discovery, or APIs as needed | `operational-insights` | All Eligible Applications | "How many datasets do I have?" · "Show me all active journeys" · "List my destinations" |
| Knowledge Graph queries | Aggregate counts, cross-entity joins, relationship lookups, and metadata exploration via single SQL queries | `knowledge-graph` | All Eligible Applications | "Which audiences use this dataset?" · "Show me relationships between schemas and datasets" |
| Experience Platform / Journey Optimizer / Customer Journey Analytics API operations | Provide a direct API gateway for mutations, real-time state checks, and entity types not in the Knowledge Graph | `cxo-api` | All Eligible Applications | "Delete dataset X" · "Check the status of my batch ingestion job" |
| Entity resolution & linking | Use semantic and lexical search to resolve entity mentions to actual Experience Platform entities and discover XDM fields | `entity-linking` | Adobe Experience Platform | "Resolve 'Holiday Shoppers' to an actual audience" · "Find me fields related to purchase history" |
| Manage custom skills | Save, modify, or delete user-owned reusable skills that persist across sessions | `manage-skill` | All Eligible Applications | "Save that workflow as a skill" · "Delete my weekly report skill" · "Turn this into a reusable skill" |

## Sandbox tooling

| Use Case | Description | Skills | Application | Sample Prompts |
| --- | --- | --- | --- | --- |
| [Move objects across sandboxes](/help/agents/sandbox-tooling.md) | Seamlessly migrate schemas, audiences, and other object configurations across sandboxes, with dependencies auto-resolved | `sandbox-tooling-workflow` | Adobe Experience Platform | "Move schema Luma Loyalty Members Platinum from current sandbox to prod sandbox" · "Promote the US Gold Loyalty Members audience to stage" |
