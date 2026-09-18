---
description: description goes here.
title: Stop a campaign
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Stop a campaign {#stop-campaign}

Users can now stop a campaign that is actively sending (a "live" campaign) directly from the campaign detail page. Stopping a campaign is permanent: recipients stop progressing through the campaign immediately, and the campaign cannot be resumed or restarted afterward.

## Prerequisites

- The campaign must be in a live (actively sending) state. The Stop action is not available for draft, scheduled, or already-stopped campaigns.
- [NEEDS INPUT — to confirm with engineer: does stopping a campaign require a specific role or permission, or can any user with campaign access do this?]

## What this feature does

A "Stop Campaign" action appears in the campaign detail header whenever a campaign is live. Selecting it opens a confirmation dialog warning that the action is permanent. Confirming calls the backend to stop the campaign; on success, the campaign's status changes to "Stopped" and a confirmation message appears.

### Key behaviors

- The Stop Campaign action only appears while a campaign is live (actively sending).
- Stopping is permanent: recipients stop progressing through the campaign and it cannot be resumed.
- A confirmation dialog requires the user to explicitly confirm before the campaign is stopped.
- After stopping, the campaign's status badge updates to "Stopped."
- If the stop request fails, an error message is shown and the campaign remains live.



### Input fields / parameters

Not applicable — this feature is a single confirmation action with no input fields.

## UI callouts

> **Tech writer note**: Screenshots needed for the following:

- [ ] The "Stop Campaign" button in the campaign detail header, shown on a live campaign
- [ ] The confirmation dialog with the permanence warning
- [ ] The "Stopped" status badge after a successful stop
- [ ] The error message shown if stopping fails

## What this feature does not do

- It does not pause a campaign temporarily. There is no way to resume a stopped campaign; stopping is a one-way action.
- It does not support restarting or relaunching a stopped campaign from the same campaign record.
- [NEEDS INPUT — to confirm with engineer: is there a separate "pause and resume" capability planned, or is Stop the only state-control action shipping in this release?]
