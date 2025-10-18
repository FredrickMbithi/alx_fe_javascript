# Dynamic Quote Generator

This app demonstrates advanced DOM manipulation, Web Storage (localStorage and sessionStorage), JSON import/export, and a simulated server sync with simple conflict resolution.

Features:
- Generate and display random quotes
- Filter by category with a dynamic dropdown
- Add new quotes and categories via a form
- Persist quotes and last-selected filter using localStorage
- Remember last viewed quote per session using sessionStorage
- Import and export quotes as JSON
- Periodic sync with a mock server (server data wins on conflicts)

How to run:
1. Open `index.html` in a browser.
2. Use “Show New Quote” to display a random quote. Select a category from the dropdown to filter.
3. Add quotes using the inputs and “Add Quote” button.
4. Export your quotes using the “Export JSON” button. Import via the file input.
5. The app periodically syncs with a mock API and will notify you when new quotes arrive.

Notes:
- All data is stored under the keys:
	- `alx_dom_quotes_v1` (quotes in localStorage)
	- `alx_dom_quotes_filter` (last filter in localStorage)
	- `alx_dom_quotes_last_quote` (last viewed quote in sessionStorage)
- Import expects an array of objects with at least `text` and `category` fields. Optional fields: `id`, `updatedAt`.
- Sync uses JSONPlaceholder posts to simulate server-provided quotes; in conflicts, server entries overwrite local ones by ID.
