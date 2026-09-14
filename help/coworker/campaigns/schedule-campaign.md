---
description: description goes here.
title: Schedule a campaign
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Schedule a campaign {#schedule-campaign}

When launching a campaign, users can now choose exactly when it goes out: immediately, at a specific future date and time, or on a repeating (recurring) schedule. Users can also come back later and change the schedule of a campaign that's already been launched or scheduled.

> **What changed**: Previously, campaigns could only be launched immediately. This release adds one-time future scheduling, recurring schedules, and the ability to edit a schedule after launch.

## Prerequisites

- The campaign must be ready to launch (all required setup complete).
- No prerequisites required beyond having a campaign in a launchable state.

## What this feature does

When a user launches a campaign, they choose one of three schedule modes, then confirm. The chosen schedule determines when the campaign starts sending and, for recurring campaigns, how often it repeats and when (or whether) it ends. Once a campaign is scheduled or live, its schedule can be edited from the campaign settings.

### Key behaviors

- Three schedule modes are available when launching: **Now**, **Schedule once**, and **Recurring**.
- A campaign scheduled for the future shows a "Scheduled" status until its start time arrives, then automatically switches to "Live."
- A recurring campaign that has started shows "Live" along with a summary of its recurrence (for example, "Weekly on Tue, Thu at 9:00 AM").
- Recurring campaigns can be set to run indefinitely ("Never" end) or until a specific end date. One-time and immediate campaigns don't have an end date option, since they run once.
- Users can edit the schedule of a campaign that has already been launched or scheduled, using the same schedule options, from the campaign's settings.

## How to use it

**To schedule a campaign at launch:**

1. From the campaign, click **Review and launch**.
2. In the launch dialog, choose a schedule option:
   - **Now** — the campaign starts sending immediately after launch.
   - **Schedule once** — pick a future **Start date** (date and time together).
   - **Recurring** — choose a **Frequency** (Daily, Weekly, or Monthly) and a start time, then set the recurrence pattern (see fields below).
3. If Recurring is selected, choose whether the campaign ends **Never** or **On a date**, and pick an end date if applicable.
4. Confirm to launch the campaign with the selected schedule.

**To edit an existing schedule:**

1. Open the campaign and go to its settings.
2. Find the schedule section and select the current schedule summary.
3. Update the schedule using the same options described above.
4. Save the change.

### Input fields / parameters

| Field | Description | Required? |
| --- | --- | --- |
| Schedule mode | Choice of Now, Schedule once, or Recurring | Yes |
| Start date | Date and time the campaign starts (Schedule once mode) | Yes, for Schedule once |
| Frequency | Daily, Weekly, or Monthly (Recurring mode) | Yes, for Recurring |
| Start time | Time of day the recurring campaign sends | Yes, for Recurring |
| Days of week | Which day(s) the campaign repeats on | Yes, for Weekly frequency |
| Day of month | Which day of the month the campaign repeats on | Yes, for Monthly frequency |
| End campaign | Never, or on a specific end date | Yes, for Recurring |



## What this feature does not do

- It does not support custom repeat intervals, such as "every 2 weeks" or "every 3 days" — only the standard Daily, Weekly, or Monthly frequencies are available.
- It does not support relative monthly recurrence, such as "the second Monday of the month" — only specific day-of-month selection is available for Monthly.
- It does not offer an end date for **Now** or **Schedule once** campaigns — an end date is only available when Recurring is selected, since one-time campaigns run once by definition.
