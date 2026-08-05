---
title: AI in CX Enterprise Applications
description: Learn how CX Enterprise applications use generative AI (GenAI), AI Assistant, agentic AI, CX Enterprise Coworker, and MCP tools.
TQID: https://experienceleague.adobe.com/heALjEZbowNaygG24oOM2HSlHa9oYVI5ViUNZDr19Ds
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# AI in CX Enterprise

This guide covers AI capabilities in Adobe CX Enterprise: generative AI, AI Assistant, Agent Orchestrator, Experience Platform Agents, CX Enterprise Coworker, and MCP.

## AI capabilities overview

Start here for a primer on where and how AI is used across CX Enterprise:

- [Generative AI](./overview/generative-ai.md) describes which CX Enterprise applications support generative AI and AI Assistant, and how they compare.
- [Agentic AI](./overview/agentic-ai.md) explains how Experience Platform Agents work in both existing CX Enterprise applications and AI-first applications, and lists the agents available in each.
- [Agentic AI monitoring](./overview/monitoring.md) covers the dashboards that track agent adoption, usage, feedback, and AI Credit consumption.
- [Agent jobs and AI credit consumption](./overview/ai-credit-consumption.md) explains how agent jobs consume AI Credits, with estimated consumption rates by agent and job type.
- [CX Enterprise agentic tools](https://experienceleague.adobe.com/en/docs/cx-enterprise-agentic-tools/using/overview) cover additional agentic skills and tooling that extend CX Enterprise agents (video tutorials).

## AI Assistant

[AI Assistant](./ai-assistant/ai-assistant-ui.md) is a conversational, generative AI tool available in Adobe Experience Platform-based applications. Use it to gain product knowledge, troubleshoot problems, find operational insights, and access Experience Platform Agents, all through natural language prompts in a full-screen or rail view interface.

To learn how to navigate the interface, read the [AI Assistant UI guide](./ai-assistant/ai-assistant-ui.md). To see example prompts by agent, see the [prompt library](./ai-assistant/prompt-library.md).

## Agent Orchestrator and Experience Platform agents

[Agent Orchestrator](./agents/agent-orchestrator.md) is the agentic layer that powers Experience Platform Agents. When you ask AI Assistant a question, Agent Orchestrator plans the work, calls on the specialized agents needed to answer it, and returns a unified response, all with human oversight.

The following Experience Platform Agents are documented in this guide:

- [Audience Agent](./agents/audience.md)
- [Data Insights Agent](./agents/cja-data-insights-agent.md)
- [Experimentation Agent](./agents/agent-experiment.md)
- [Field Discovery Agent](./agents/field-discovery-agent.md)
- [Journey Agent](./agents/ajo-agent.md)
- [Notifications Agent](./agents/notifications.md)
- [Product Support Agent](./agents/product-support.md)
- [Adobe Marketing Agent for Microsoft 365 Copilot](./agents/ama-ms.md)
- [Validate your data](./agents/data-validation.md)

For the full list of agents, the applications each supports, and eligibility requirements, see [Agentic AI in CX Enterprise](./overview/agentic-ai.md).

## Coworker

Coworker is an agent-first evolution of AI Assistant that automates customer experience and marketing workflows, so your team can focus on business goals instead of routine execution. Instead of asking one question at a time, you describe a goal. Coworker plans, executes, validates, and returns the finished work for your approval. Coworker includes:

- **[Coworker Chat](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/overview)**: A conversational interface for exploring your data, validating audiences and journeys, and completing multi-step tasks across CX Enterprise applications.
- **[Coworker Campaigns](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/campaigns/overview)**: An AI-native application that consolidates campaign briefing, audience building, content generation, journey design, and proofing into a single conversational experience. It uses built-in templates, best practices, and prompting guidance to help small, agile teams launch campaigns quickly.
- **Coworker Projects** (coming soon): A unified workspace for automating end-to-end customer experience orchestration workflows, helping teams coordinate tasks, approvals, and execution to drive outcomes from strategy through delivery. Documentation for Projects is coming soon.

Eligible customers are gradually being transitioned from AI Assistant and Experience Platform Agents to Coworker Chat. Read [Coworker Trial](./agents/trial.md) to learn about trial eligibility, AI Credit usage, and how to get access.

To see Coworker Chat in action, walk through [Coworker Chat in Playground](./coworker/playground-coworker-chat.md), or read real-world use cases such as [Validate AA to CJA migration data](./coworker/data-validation-aa-cja.md) and [Analyze CJA data](./coworker/chat/analytics-chat.md).

For full product documentation on Coworker Chat, Campaigns, and Projects, see [Coworker](./coworker/overview.md). For sandbox-to-sandbox object replication, see [Sandbox Tooling Agentic Skills](./agents/sandbox-tooling.md).

## MCP

[Adobe CX Coworker Gateway](./mcp/overview.md) is the unified Model Context Protocol (MCP) endpoint for CX Enterprise. It gives MCP-compatible clients, such as [!DNL Claude], [!DNL ChatGPT], and [!DNL Cursor], a single governed connection to the product tools your organization is entitled to use. These tools include [!DNL Real-Time CDP], [!DNL Experience Platform], [!DNL Journey Optimizer], [!DNL Customer Journey Analytics], [!DNL Adobe Analytics], and [!DNL Workfront].

New to CX Coworker Gateway? See [Access CX Coworker Gateway tools](./mcp/access.md) and [Install CX Coworker Gateway](./mcp/install.md) to get connected.

## Get started

### Access requirements

Your Adobe Admin must grant the appropriate permissions before you can use AI Assistant and Experience Platform Agents. Requirements vary by application; see [Access](./agents/agent-orchestrator.md#access) in the Agent Orchestrator guide for details.

### Privacy and security

AI Assistant and Experience Platform Agents prioritize privacy, security, and governance, including sandbox-specific data isolation and your existing access control policies. For full details, read [Privacy, security, and governance in AI Assistant](./ai-assistant/privacy.md).

## Best practices

To get the most value from your AI Assistant or Coworker experience, follow these best practices:

- **Be specific** in your prompts to obtain targeted and relevant insights.
- **Verify responses** by reviewing the source citations and reasoning explanations provided.
- **Use context setting** to make sure the most relevant data sources are used for your questions.
- **Provide feedback** to help improve performance and accuracy over time.
- **Combine insights** from multiple agents for a more comprehensive analysis.

## Legal considerations

AI Assistant currently supports responses in English only, and language models occasionally make mistakes. Always verify the information provided, and use the reasoning steps included in each response to understand how it was generated. For full details, read the [legal disclaimer](./ai-assistant/legal-disclaimer.md).

