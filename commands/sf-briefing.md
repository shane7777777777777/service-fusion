---
description: "Morning operations briefing — today's jobs, missed calls, open estimates, dispatch capacity, on-call tech"
allowed-tools:
  - "mcp__servicefusion__*"
---

# Morning Operations Briefing

Pull a complete morning briefing from Service Fusion for Phoenix Electric.

## Instructions

Execute these API calls in order, then format as an executive summary:

1. **Today's Jobs:** Call `sf_get_daily_job_summary` with today's date (YYYY-MM-DD format). Report total jobs, breakdown by status (Pending/Scheduled/Dispatched/Working/Completed), and list any Urgent/High priority jobs.

2. **Missed Calls:** Call `sf_get_missed_calls` with `since` set to the last business day (skip weekends). Report count and list caller info.

3. **Open Estimates:** Call `sf_list_estimates` with `status: "Open"`. Report count and total dollar value if available.

4. **Dispatch Capacity:** Call `sf_get_capacity` with today's and tomorrow's date. Report available slots.

5. **On-Call Technician:** Call `sf_get_on_call_technician`. Report who's on call.

## Output Format

Present as a clean summary table with sections for each area. Highlight urgent items. End with recommended actions for the day.
