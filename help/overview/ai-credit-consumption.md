---
title: AI Credit Consumption
description: Learn about AI credits consumption in CX Enterprise applications.
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
    internal-label: AI Tools
---
# AI credits consumption

Learn about AI credits consumption in CX Enterprise applications. 

## AI credits

An _AI credit_ is a usage-based metric that quantifies the execution of actions or jobs. 

## Eligible services consuming AI credits

* [CX Enterprise Coworker](#cx-enterprise-coworker-credit-rate)
* [AEP Agents](#aep-agents-credit-rate)

### CX Enterprise Coworker credit rate

For a limited introductory period, Coworker inputs consume AI credits at a rate of 25 AI credits per Input. This rate is available for a limited time only and is subject to change.

### AEP Agents credit rate

An _agent job_ is a series of tasks and actions an AEP agent executes to achieve a specific outcome, as directed by customer inputs.

Using natural language prompts via AI Assistant, you can ask agents to carry out specific jobs. Based on those inputs, Agent Orchestrator coordinates the appropriate agents to execute each step within the relevant CX Enterprise applications.

AI credit usage may vary depending on the complexity and value of the job executed:

* Simple (often single-step) tasks consume fewer credits  
* Complex (often multi-step) tasks consume more credits  
* Tasks involving advanced reasoning, validation, multi-agent coordination, or integration consume more credits  

To see which AEP Agents and agent jobs are available in your licensed CX Enterprise apps, see [CX Enterprise Agentic AI Capability Catalog](https://agentic-capability-explorer.entapp.adproto.com/).

#### Estimated agent job credit rates

| Agent | Job | Supported applications | Estimated AI credits | Sample prompts |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience Agent | Audience / account ideation | <ul><li>Real-Time CDP (B2B, B2C, and B2P Editions)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li><em>Show me fields for affluent buyers</em></li><li><em>Find all fields related to customer preferences</em></li></ul> |
| Audience Agent | Audience / account management | <ul><li>Real-Time CDP (B2B, B2C, and B2P Editions)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>Do I have any duplicate audiences?</em></li><li><em>Show me my 5 largest audiences.</em></li><li><em>Show me audiences that are not activated to any destination</em></li><li><em>List all audiences used in live journeys</em></li></ul> |
| Audience Agent | Audience / account analysis | <ul><li>Real-Time CDP (B2B, B2C, and B2P Editions)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>Which audiences have increased in size by more than 20% in the last week?</em></li><li><em>How much has audience "Loyal Platinum" changed compared to the value 30 days ago?</em></li><li><em>What is my fastest growing audience?</em></li></ul> |
| Audience Agent | Buying group ideation | <ul><li>Adobe Journey Optimizer (B2B Edition)</li></ul> | 25 | <ul><li><em>Which accounts are showing intent for these products?</em></li><li><em>Show me the top persons by product intent for XYZ.</em></li><li><em>Which buying groups have more than 5 members?</em></li></ul> |
| Data Insights Agent | Data analysis and visualization | <ul><li>Customer Journey Analytics (B2C and B2B Editions)</li></ul> | 25 | <ul><li><em>Trend orders in July</em></li><li><em>Show revenue by region.</em></li><li><em>Show orders by gender, from March to June.</em></li><li><em>What were my top 10 SKUs by profit in June</em></li><li><em>Proportion of purchases by month of year</em></li><li><em>Share of revenue by product category</em></li></ul> |
| Journey Agent | Journey ideation | <ul><li>Adobe Journey Optimizer (B2B Edition)</li></ul> | 25 | <ul><li><em>Create a journey for whitespace accounts with intent for my solution, focusing on people engaged with content on the website</em></li></ul> |
| Journey Agent | Journey analysis | <ul><li>Adobe Journey Optimizer (B2B and B2C Editions)</li></ul> | 50 | <ul><li><em>I want to analyze the fallout by node for journey Fourth of July Campaign.</em></li><li><em>Are there any scheduling conflicts for journey X</em></li><li><em>Show me audience overlap conflicts for journey X</em></li></ul> |
| Journey Agent | Journey management | <ul><li>Adobe Journey Optimizer (B2B and B2C Editions)</li></ul> | 25 | <ul><li><em>How many live journeys do I have?</em></li><li><em>List all journeys using the audience X.</em></li><li><em>List all journeys currently in test mode</em></li></ul> |
| Product Support Agent | Knowledge-based troubleshooting | <ul><li>Real-Time CDP (B2B, B2C, and B2P Editions)</li><li>Adobe Journey Optimizer (B2C and B2B Editions)</li><li>Customer Journey Analytics (B2C and B2B Editions)</li></ul> | 0 | <ul><li><em>Why does my profile count differ on the License Usage Dashboard and the Experience Platform home page?</em></li><li><em>What are the reasons for a journey not triggering?</em></li><li><em>How does Adobe Experience Platform create real-time experiences?</em></li><li><em>How do you configure and use alerts in Adobe Experience Platform?</em></li><li><em>What is the average profile richness limit in Adobe Experience Platform Activation?</em></li></ul> |
| Product Support Agent | Support case creation and tracking | <ul><li>Real-Time CDP (B2B, B2C, and B2P Editions)</li><li>Adobe Journey Optimizer (B2C and B2B Editions)</li><li>Customer Journey Analytics (B2C and B2B Editions)</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em>Create a new support ticket for my failing segmentation job</em></li><li><em>What's the status of ticket E-001772068?</em></li></ul> |
| Content Advisor Agent | Content discovery | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>Show content fragments for creating WKND offer campaign.</em></li><li><em>Find product packaging PNG images.</em></li><li><em>Show images tagged office in folder WKND.</em></li><li><em>Are there any svgs in folder WKND?</em></li><li><em>Show me all loan application forms.</em></li><li><em>I'm looking for employee onboarding forms.</em></li></ul> |
| Content Advisor Agent | <ul><li>Content optimization</li></ul> | <ul><li>Adobe Experience Manager Assets and Dynamic Media</li></ul> | 10 | <ul><li><em>Create a 2000px rendition as JPEG with 80% quality.</em></li><li><em>Create a rendition for an Instagram story.</em></li><li><em>Overlay the image with 30% discount graphics over the promotional banner, placing it 100px from the center.</em></li><li><em>Change background color of the PNG to #ff8932.</em></li></ul> |
| Brand Governance Agent | <ul><li>Brand policy checks</li></ul><ul><li>Permissions with Content Hub</li></ul><ul><li>Asset expiration</li></ul> | <ul><li>Adobe Experience Manager Sites (Brand Policies)</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em>Is this page aligned with my brand? `https://www.website/en.html`</em></li><li><em>Show all existing Content Hub ABAC rules</em></li><li><em>Are any of my assets expiring soon?</em></li></ul> |
| Brand Experience Agent | <ul><li>Content update</li><li>Forms creation</li><li>Pipeline troubleshooting</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>On `URL`, update the headline to Hello world</em></li><li><em>Build a contact form with name, email and message fields</em></li><li><em>Troubleshoot my failed pipeline</em></li><li><em>List my failed pipelines for Main Program.</em></li></ul> |
| Brand Experience Agent | Site modernization | Adobe Experience Manager Cloud Services | 100 | <ul><li><em>Migrate the page `https://wknd-trendsetters.site`</em></li></ul> |

>[!NOTE]
>
>Actual AI credit consumption may vary depending on the number of steps executed and iterations per step. 

## More help on this topic

* [GenAI in CX Enterprise](generative-ai.md)
* [Agentic AI in CX Enterprise](agentic-ai.md)
* [Adobe Experience Platform Agents usage-bound trial](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/agents/trial)
