---
title: Agentic AI in CX Enterprise Applications
description: Learn where agentic AI is available in CX Enterprise applications.
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
    internal-label: AI Tools
---
# About Agentic AI in Adobe CX Enterprise

Adobe [Experience Platform Agent Orchestrator](../agents/agent-orchestrator.md) powers agentic AI capabilities in CX Enterprise applications.

Agents help automate tasks, deliver insights faster, and streamline workflows. As a result, teams can work more efficiently and get more value from CX Enterprise.

CX Enterprise AI agents are available in either:

* [Existing CX Enterprise applications](#existing-apps)
* [AI-first CX Enterprise applications](#ai-first-apps)

The following sections describe these two ways to enable agentic AI in CX Enterprise.

## Existing CX Enterprise applications {#existing-apps}

In existing applications, you can use natural language to instruct Adobe Experience Platform Agents through the conversational interface in [AI Assistant](../ai-assistant/ai-assistant-ui.md). AI Assistant is available in both full-screen and right-rail views.

Agents can be enabled in existing CX Enterprise apps for customers in one of the following categories:

* You purchased an Adobe Experience Platform Agents AI Credits license
* You are included in a usage-bound trial (limited AI Credits provided)
* You transacted the Agent Orchestrator Promo SKU (time-bound trial license)

Using AI agents to perform _agent jobs_ consumes AI credits. Learn more about agent jobs and AI credits in _[Agent jobs and AI credit consumption](ai-credit-consumption.md)_.

AI agents follow _your_ input and oversight, and they respect product-level access controls. You can only perform jobs or access data that you are authorized to use in the underlying CX Enterprise application.

### AI agents in existing CX Enterprise apps {#existing-apps-table}

The following table lists Experience Platform Agents available in existing CX Enterprise applications. 

| Agent name  | Capabilities | Supported applications | Health Data / HIPAA-ready |
|---|----------|----------|----------|
| [Audience Agent](../agents/audience.md)  | Empower your teams to manage and optimize audiences using natural language prompts for greater ease, efficiency, and speed to market. |<ul><li>Real-Time CDP (B2B, B2C, and B2P editions)</li><li>Adobe Journey Optimizer (B2B and B2C editions)</li></ul> | |
| [Content Advisor Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-advisor/overview) | <ul><li>Helps teams quickly find the most relevant content across the enterprise using natural language, reducing time spent searching and enabling faster decisions and execution.</li><li>Simplify creating visual content variants from source assets using natural language prompts.</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul><ul><li>Dynamic Media (Cloud Services)</li></ul> | |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai)  |  Quickly answers questions about your data. It builds relevant visualizations in Analysis Workspace using components from your data view and using your actual data. | <ul><li>Customer Journey Analytics (B2B and B2C Editions)</li></ul>  | Yes |
| [Brand Experience Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/overview) |<ul><li>Accelerates the migration and modernization of digital experiences by automatically restructuring, enriching, and validating existing sites so teams can move faster to modern, AI-ready experiences with less risk and manual effort.</li><li>Takes on high-volume experience creation and updates, dramatically reducing manual effort and cycle time so teams can move faster without sacrificing quality or consistency.</li><li>Speeds up the creation of optimized, on-brand forms by generating, structuring, and validating form experiences automatically, enabling teams to launch faster and capture higher-quality data with minimal manual effort.</li><li>Helps AEM CS developers and technical administrators troubleshoot build-step failures in the Cloud Manager pipeline by analyzing the root cause and suggesting fixes.</li></ul> | <ul><li>Adobe Experience Manager Sites Cloud Services (Experience Modernization)</li></ul><ul><li>Adobe Experience Manager Sites (Experience Production)</li></ul><ul><li>Adobe Experience Manager Forms (Form Creation)</li></ul><ul><li>All cloud-based Adobe Experience Manager applications (Development Support)</li></ul> | |
| [Brand Governance Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview) | Safeguard brand integrity and compliance with automated brand policies checks, permissions, intelligence to support DRM with real-time governance. | <ul><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Sites (Brand Policy)</li></ul> | |
| [Journey Agent](../agents/ajo-agent.md) | Enable your teams to quickly analyze and optimize multi-touch customer journeys at scale. | <ul><li>Adobe Journey Optimizer (B2B and B2C editions)</li></ul> | |
| [Product Support Agent](../agents/product-support.md) | Troubleshoot support issues without leaving your workflows, create customer support tickets, and track case progress using AI Assistant. | <ul><li>Real-Time CDP (B2B, B2C, and B2P Editions)</li><li>Adobe Journey Optimizer (B2B and B2C Editions)</li><li>Customer Journey Analytics (B2B and B2C Editions)</li><li>Adobe Experience Manager</li></ul> | |
| [Adobe Marketing Agent for Microsoft 365 Copilot](../agents/ama-ms.md) | Connects Experience Platform directly to Microsoft 365 Copilot. You can ask natural-language questions within Microsoft 365 applications, such as Teams, Word, Powerpoint, and Excel to instantly retrieve marketing insights from Experience Platform without interrupting your workflow. | <ul><li> Adobe Agent Orchestrator with support for Audience Agent, Journey Agent, Customer Journey Analytics Data Insights, Experience Platform Operational Insights</li></ul> | |

## AI-first CX Enterprise applications {#ai-first-apps}

AI-first applications are built with generative or agentic AI as the primary component. They use generative or agentic AI for key tasks, and the agentic features are already included in the AI-first application license. As such, they do not require the Experience Platform Agent Orchestrator license.

The following table lists Experience Platform Agents available as AI-first applications. They are enabled by licensing these AI-first applications:  

| Agent name  | Capabilities | Supported applications   |
|---|----------|----------|
| [CX Enterprise Coworker](../coworker/overview.md) | Acts as an agentic teammate: plans multi-step work from a natural-language goal, executes it across your Adobe and connected systems, validates the results, and returns the finished work for your approval — reducing the need to coordinate tasks manually. | <ul><li>CX Enterprise Coworker (Chat)</li><li>CX Enterprise Coworker (Campaigns)</li></ul> |
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) |  Automate, analyze, and synthesize insights, so you can quickly identify high-impact experiments and growth opportunities from a centralized workspace — all while reducing manual processes.  | <ul><li>AJO Experimentation Accelerator</li></ul>   |
| [LLM Optimization Agent](https://experienceleague.adobe.com/en/docs/llm-optimizer/using/home) |  Enhance visibility, accuracy, and influence in AI-driven search environments, provide insights into brand presence in AI-generated answers, offer prescriptive content recommendations, and automate optimization fixes. | <ul><li>Adobe LLM Optimizer</li></ul>   |
| [Site Optimization Agent](https://experienceleague.adobe.com/en/docs/experience-manager-sites-optimizer/content/home) | Maximize business impact by automatically detecting and deploying website enhancements. Using generative AI and multiple monitoring technologies, you can increase site traffic acquisition, engagement, and more | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) |  Boost conversion and engagement through intelligent, context-aware product discovery tailored to individual preferences and behaviors. | <ul><li>Adobe Brand Concierge</li></ul> |

## More help on this topic

* [CX Enterprise Agentic Tools](https://experienceleague.adobe.com/en/docs/cx-enterprise-agentic-tools/using/overview#adobe-cx-enterprise-agentic-tools)
* [Agent jobs and AI credit consumption](ai-credit-consumption.md)
* [AI documentation home](https://experienceleague.adobe.com/en/docs/ai) documentation home
* [Overview of Agents in Experience Manager as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE Learn more on Adobe for Business]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="Go to Business.adobe.com"}
