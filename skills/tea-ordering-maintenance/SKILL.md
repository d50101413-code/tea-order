---
name: tea-ordering-maintenance
description: Maintain the tea ordering page when its staff roster, drink choices, customizations, ordering rules, or deadline changes.
---

# Tea Ordering Maintenance

Use this skill when updating the tea ordering page in the current workspace or a follow-up version of it.

## Working rules

- Locate the active ordering page and its source files before editing. In this workspace the page is `index.html`.
- Treat the current personnel list and drink menu as changeable data. Use the latest file or list supplied for the task; do not preserve removed names or options just because they appeared in an earlier version.
- Keep each roster or menu choice in one source of truth, then make the ordering UI, progress list, per-person summary, aggregate summary, and CSV downloads use that same data.
- The current policy is one drink per person. Prevent duplicate orders for a person, show their status as not ordered, ordering, or complete, and keep order changes possible by removing the existing order before re-entry. Change this policy only when the user asks.
- The current menu has tea, sugar, ice, and optional topping choices. When an option is added, renamed, or removed, update the choices, displayed order details, aggregation key, and exported columns or values as needed.
- For a requested ordering window, use the user's stated start and end. If they say a duration from now, anchor a fixed deadline at the request time in Asia/Taipei and show that exact cutoff in the page. Disable name entry, drink choices, and order submission at expiry while keeping existing orders and exports available.
- Keep the staff progress list useful for identifying people who have not ordered. If the roster changes, update the displayed roster count and progress denominator from the roster data rather than leaving stale hard-coded counts.
- Keep labels and guidance in Traditional Chinese, matching the existing page.

## Workflow

1. Inspect the current page and any newly supplied roster or menu source.
2. Update the roster, menu, rules, and deadline only within the requested scope.
3. Check that every changed option appears in the form, individual order view, aggregated totals, and relevant CSV output. Check that the roster count and order status cover the full current roster.
4. Report the changed behavior and any remaining assumptions, such as a missing deadline time or unspecified prices.

