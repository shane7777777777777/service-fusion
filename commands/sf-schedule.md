---
description: "View today's and tomorrow's schedule — appointments, technician availability, on-call"
allowed-tools:
  - "mcp__servicefusion__*"
---

# Schedule View

Display the current dispatch schedule from Service Fusion.

## Instructions

1. Call `sf_list_appointments` with `startsOnOrAfter` set to today's start (00:00:00Z) and a reasonable end range
2. Call `sf_list_technician_shifts` for today and tomorrow
3. Call `sf_get_on_call_technician`
4. Call `sf_get_capacity` for today and tomorrow

Present appointments grouped by technician, showing time slots, customer names, job types, and any gaps in coverage. Highlight the on-call tech and overall capacity.
