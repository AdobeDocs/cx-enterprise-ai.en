---
description: description goes here.
title: Launch a campaign
---
# Launch a campaign {#launch-campaign}

Launching a campaign is the action that moves it from draft to active sending. Before the launch dialog opens, Halo checks that the campaign is ready and blocks launch until required setup is complete. The launch dialog shows a preview of the email and audience, lets the user review or change the send schedule inline, and reports back whether the launch succeeded. This section covers the end-to-end launch experience; for the schedule options offered during launch, see [Schedule a campaign](/help/coworker/campaigns/schedule-campaign.md).

## Prerequisites

- The campaign must be in Draft status. <!-- The Launch action isn't available once a campaign is already live. -->
<!-- - The campaign must pass a readiness check: sending settings configured, at least one test email sent, and a real (non-sample) audience uploaded. -->
- [NEEDS INPUT — to confirm with engineer: some users may see a "coming soon" experience instead of a real Launch button, which only offers downloading the campaign or sending a proof email rather than launching in-app. Confirm what determines which experience a given user or campaign gets.]

## What this feature does

When a user launches a campaign, Halo first validates that the campaign is ready. If anything required is missing, a dialog lists what needs to be fixed before launch can proceed. Once validation passes, the launch dialog shows a preview of the email and audience/workflow, lets the user review or edit the send schedule without leaving the flow, and — for large sends — shows an estimated send-volume notice. Confirming triggers the launch, and Halo reports one of three outcomes: launched, already launched, or failed.

### Key behaviors

- Launch is only available for campaigns in Draft status; a campaign that's already live can't be launched again.
- A readiness check runs automatically before the launch dialog opens. Unresolved issues block launch and are listed with a way to resolve each one.
- The launch dialog shows an email preview (subject, preheader, sender) and an audience/workflow preview.
- The send schedule can be reviewed or changed from inside the launch dialog.
- For large sends, the dialog shows an estimated send-volume impact. [NEEDS INPUT — exact wording of this notice wasn't available from code]
- On success, the campaign's status updates to "Scheduled" or "Live" (depending on the chosen schedule), and a confirmation message notes that campaign insights will be available within 2 hours.
- If the campaign was already launched (for example, from a duplicate click), Halo shows an "already launched" message rather than an error.
- If launch fails, an error message appears and the campaign stays in Draft; the user can try again.
- Once a campaign is stopped <!--(see [Stop a live campaign](./stop-live-campaign.md))-->, it can't be relaunched from the same campaign record — stopping is a separate, permanent state.

## How to access

**To launch a campaign:**

1. From the campaign, click **Launch** (shown as "Ready to launch" while still in draft).
2. If anything is missing, a dialog titled "A few things still need attention" lists what to complete:
   - **Configure email settings** — sending parameters (sender/domain) haven't been set up yet.
   - **Emails not tested** — send at least one test email to proof the email before launch.
   - **Real audience required for launch** — the campaign is still using a sample audience; upload a real audience CSV.
   Resolve each item, then try Launch again.
3. Once the campaign passes the readiness check, the launch dialog opens, showing a preview of the email and audience.
4. Review the schedule shown in the dialog. To change it, use the schedule options described in [Schedule when a campaign launches](/help/coworker/campaigns/schedule-campaign.md), then save.
5. Confirm to launch. On success, a confirmation message appears and the campaign's status updates (to "Scheduled" or "Live").

<!-- 
## Input fields / parameters

Not applicable beyond the schedule fields already documented in [Schedule when a campaign launches](/help/coworker/campaigns/schedule-campaign.md) — launching itself doesn't require any additional input. 
-->

## UI callouts

> **Tech writer note**: Screenshots needed for the following:

- [ ] The Launch entry point/button in the campaign detail header
- [ ] The readiness/validation dialog listing incomplete items
- [ ] The launch dialog showing the email + audience preview and the schedule section
- [ ] The estimated send-volume impact notice (for large audiences)
- [ ] The success confirmation message after launch
- [ ] The "already launched" message
- [ ] The generic launch-failure error message

## What this feature does not do

- It doesn't let a campaign launch with a sample (non-real) audience, untested emails, or unconfigured sending settings — all three must be resolved first.
- Launching doesn't accept a schedule as part of the same action; the schedule is saved separately (from within the same dialog) before or as part of confirming launch.
- It doesn't support relaunching a campaign that's been stopped — stopping is permanent <!--(see [Stop a live campaign](./stop-live-campaign.md))-->.
- [NEEDS INPUT — to confirm with engineer/PM: for some users, Launch may be replaced by a "coming soon" experience offering only a campaign download (PDF/DOCX) or a proof email send, without in-app self-serve launch. Confirm the audience this applies to before publishing, since it changes the how-to steps for that cohort.]
