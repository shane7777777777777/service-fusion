---
description: "Build estimates and proposals — guided workflow with pricebook integration"
allowed-tools:
  - "mcp__servicefusion__*"
  - Write
---

# Estimate Builder

Guided estimate creation with pricebook integration and document generation.

## Instructions

Walk through the estimate creation process:

1. **Identify customer:** Ask for customer name/ID. Use `sf_search_customers` to find them.
2. **Select or create job:** Use `sf_list_jobs` for the customer. If no active job, offer to create one with `sf_create_job`.
3. **Browse pricebook:** Use `sf_list_services`, `sf_list_materials`, and `sf_list_equipment` to help the user select line items. Filter by category with `sf_list_categories`.
4. **Build line items:** Assemble description, quantity, and unit price for each item. Apply Phoenix Electric pricing tiers if applicable.
5. **Review:** Present the complete estimate with subtotal, any markup, and total.
6. **Create in SF:** Use `sf_create_estimate` with the assembled data. Confirm before creating (write operation).
7. **Document (optional):** If requested, generate a formatted proposal/estimate document as markdown and write to a file. Include Phoenix Electric branding, scope of work, terms, and pricing table.
