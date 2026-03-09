---
description: "Job management — list, create, update, cancel jobs, view daily summary"
allowed-tools:
  - "mcp__servicefusion__*"
---

# Job Management

Manage jobs in Service Fusion — list, create, cancel, reschedule.

## Instructions

Ask the user what they need:
- **List jobs:** Use `sf_list_jobs` with optional filters (status, customerId, technicianId, date range)
- **Job details:** Use `sf_get_job` with job ID
- **Daily summary:** Use `sf_get_daily_job_summary` with date
- **Create job:** Use `sf_create_job` — needs customerId, locationId, jobTypeId, priority, summary. Look up job types with `sf_list_job_types` first. Confirm before creating (write operation).
- **Cancel job:** Use `sf_cancel_job` with reason. Confirm before canceling (write operation).
- **Reschedule:** Use `sf_reschedule_appointment` — needs appointmentId, new start/end times. Confirm before rescheduling (write operation).

Present jobs in a table with status, customer, technician, priority, and dates.
