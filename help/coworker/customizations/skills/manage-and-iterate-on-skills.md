---
title: Manage and Iterate on Skills in Coworker
description: Learn how to manage reusable AI skills with a governance workflow, establish a baseline, make controlled updates, validate improvements, and retire obsolete skills.
role: User, Developer
level: Beginner, Intermediate
doc-type: Feature Video
duration: 258
last-substantial-update: 2026-09-16
jira: KT-22445
---

# Manage and iterate on skills in [!DNL Coworker]

Reusable AI skills help teams perform consistent, repeatable tasks. As business requirements evolve, however, those skills need to evolve too. This video demonstrates a practical approach to managing the complete lifecycle of governance-focused AI skills, from evaluation and improvement to validation and retirement.

>[!VIDEO](https://video.tv.adobe.com/v/3503566/?learn=on)

## Why a Baseline Matters

Before modifying a skill, it is important to understand how the current version performs. Establishing a baseline allows you to:

- Measure the impact of future changes
- Separate skill behavior changes from underlying data changes
- Validate whether improvements actually provide better outcomes
- Maintain confidence in governance and compliance workflows
 
The video demonstrates how to run an existing skill, capture its output, and save the results for future comparison.

## Making Controlled Skill Improvements

Skill improvements should be intentional and measurable.

In this example, the Audience Quality Check skill is enhanced by:

- Adding severity classifications for identified issues
- Requiring compliant replacement names for naming violations
- Preserving existing validation checks
- Maintaining read-only behavior to prevent unintended changes

The walkthrough highlights the importance of improving a skill without altering its core governance responsibilities.

## Validating Skill Changes
 
After updating a skill, the next step is verification.

The video shows how to:

1. Re-run the revised skill against the same environment.
2. Compare the new output against the original baseline.
3. Identify whether differences were caused by:
    - Changes in audience data
    - Changes in skill instructions
    - A combination of both

This comparison process helps ensure that updates make outputs more actionable, more consistent, and more aligned with organizational standards.

## Governance Best Practices
 
Effective governance skills should:

- Clearly define their scope and responsibilities
- Produce structured and consistent outputs
- Recommend actions without making unauthorized changes
- Remain read-only when used for evaluation and compliance purposes
- Be reviewed and tested before deployment

The video demonstrates how these practices help maintain trustworthy and predictable AI-assisted workflows.

## Retiring Obsolete Skills

Skill management also includes cleanup.

When a temporary or draft skill is no longer needed, it should be carefully removed to avoid confusion and duplication. The video demonstrates:

- Confirming the correct skill before deletion
- Protecting approved production skills
- Removing experimental versions when testing is complete
- Verifying that required skills remain available after cleanup

## Key Takeaways

Successful AI skill management follows a repeatable process:
 
1. Understand the current skill definition.
2. Capture a baseline.
3. Make one change at a time.
4. Compare results against the original output.
5. Keep governance skills read-only when appropriate.
6. Remove obsolete skills responsibly.
7. Continuously align skills with current business needs.

By following these practices, teams can keep their AI skills accurate, reliable, compliant, and ready to evolve alongside changing workflows.
