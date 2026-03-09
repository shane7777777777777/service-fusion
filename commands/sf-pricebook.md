---
description: "Pricebook management — browse, update, Rexel sync, create services and materials"
allowed-tools:
  - "mcp__servicefusion__*"
---

# Pricebook Operations

Manage Phoenix Electric's Service Fusion pricebook — browse, update, create, and sync with Rexel.

## Instructions

Ask the user what they need:
- **Browse:** Use `sf_list_services`, `sf_list_materials`, `sf_list_equipment`. Filter by `sf_list_categories`.
- **Rexel price comparison:** Use `sf_compare_prices` with vendor pricing data. Input format: array of `{code, newPrice, newCost}`. Shows increases, decreases, and items not found.
- **Update material:** Use `sf_update_material` to change price, cost, name, or active status. Confirm before updating (write operation).
- **Create material:** Use `sf_create_material` with name, code, price, cost, vendor. Confirm before creating (write operation).
- **Build service from Rexel parts:** Look up Rexel materials, calculate Phoenix markup, assemble into a new pricebook service with labor + materials + equipment line items.

For Rexel integration details, read `references/rexel-integration.md` in the servicefusion-operations skill.
