---
title: Build and Run a Quality Gate Skill in Coworker
description: Learn how to use a custom Coworker skill to automatically validate audience activations against suppression lists, frequency caps, and naming standards before deployment.
role: User
level: Beginner, Intermediate
doc-type: Feature Video
duration: 101
last-substantial-update: 2026-09-08
jira: KT-22379
---

# Build and run a quality gate skill using custom AI skills

Marketing teams rely on rules and governance processes to ensure audiences are activated correctly. Before launching an audience to a destination, teams often need to verify suppression lists, frequency caps, consent requirements, and naming conventions.
 
The challenge is that these checks frequently depend on tribal knowledge and manual reviews. When processes live in people's heads, mistakes can happen.

In this video, you'll see how a custom Coworker skill acts as an Activation Gate, automatically validating audiences against your organization's activation standards before they move downstream.

>[!VIDEO](https://video.tv.adobe.com/v/3503162/?learn=on&enablevpops)

## Sample activation quality gate skill
 
You can create your own reusable **Activation Quality Gate** skill by pasting a prompt into Coworker. Coworker's skill-authoring capabilities convert the prompt into a saved skill within **your own environment**. A sample based on the video demonstration follows.
 
The key is to define **your own pass/fail standards** for the three governance gates:
 
1. Suppression / Consent
2. Frequency Cap
3. Naming Convention
 
The framework remains the same for everyone. Customize the sections marked with **`[...]`** to match your organization's standards.

## Master prompt

> **Save this as a skill called "Activation Quality Gate."**

```text
It's a governance gate that runs a pre-activation checklist before any audience is sent to a destination.

It is read-only. It never activates, mutates, or copies anything.

Resolve the named audience and destination from our Knowledge Graph, evaluate the three gates below, then render one visual scorecard containing:

- An Alert banner
- One MetricCard per gate
- A DataTable with:
- Gate
- Status
- Finding
- Required Fix

Provide a single verdict:

- CLEARED only if all three gates pass
- BLOCKED if any gate fails

For every failed gate, provide the specific remediation needed.
 
All gates fail closed:

- Missing data = BLOCKED
- Never assume success when information is unavailable
 
Trigger phrases:

- "run the activation gate"
- "is this audience ready to activate"
- "pre-activation checklist"
- "can I activate to ..."

The three gates are:
 
[Paste Gate 1, Gate 2, and Gate 3 definitions here]

```

## Gate 1: Suppression / Consent
 
> Edit this section to match your organization's suppression and consent requirements.
 
```text

Gate 1 – Suppression List

Pass only if a recognized suppression, opt-out, or consent audience is applied alongside the target audience.

Discover eligible lists using name patterns such as:

- suppress
- opt-in
- opt out
- consent
- do not contact
 
Because suppression lists may live in destination dataflows rather than audience metadata, require the marketer to confirm one is attached.
 
If no suppression or consent list exists anywhere in the sandbox, fail hard.
 
Our standard:

[Example: A consent audience is mandatory for all email and SMS destinations. For direct mail destinations it is optional.]
```

## Gate 2: Frequency Cap

> Edit this section to match your organization's delivery-frequency requirements.

```text
Gate 2 – Frequency Cap
 
Read the delivery frequency on the resolved destination.

Pass if:

- Frequency is present
- Frequency is bounded

Fail if:

- Frequency is blank
- Frequency is unbounded

Our standard:

[Example: Frequency must be DAILY or less frequent. Any hourly cadence or blank value is blocked.]

```

## Gate 3: Naming Convention
 
> Edit this section to match your organization's audience naming rules.
 
```text
Gate 3 – Naming Convention

Evaluate the audience name programmatically.

Any rule violation causes failure.

Block names that:

- Contain "test"
- Contain "copy"
- Contain an auto-copy suffix such as _[6-hex]
- Contain timestamps
- Contain 24-character object IDs
- Start with a bare number or cryptic short code
- Are entirely lowercase
- Are excessively short or unclear
- Use generic defaults such as:
- Save audience
- Email
- New Accounts
- Lack a category–qualifier separator

Our standard:

[Example: [Line of Business] – [Criteria] in title case]

Example:

Mortgage – High Propensity Prospects

When blocked on naming, always propose a compliant replacement name.

```

## Guidance 

### 1. Customize only the bracketed sections

Only update only the sections contained in **`[...]`**.
 
These sections define the organization's specific governance standards.
 
Everything else should remain unchanged:

- Audience resolution
- Gate evaluation
- Scorecard rendering
- Verdict logic


### 2. Verify Prerequisites
 
This skill depends on:
 
- Knowledge Graph access
- Audience discovery
- Destination discovery
- Suppression-list discovery
- Visual artifact support
- Alert banner
- MetricCards
- DataTable rendering

If these capabilities are not available in the customer's environment, the skill cannot run as designed.

### 3. Keep the Skill Read-Only

The skill should always remain read-only.

Include this requirement explicitly in the prompt to ensure the skill is never confused with an activation workflow.

The Activation Quality Gate evaluates activation readiness only. It does **not** activate audiences, modify configurations, or copy data.
