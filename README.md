# Dandy's World Nuzlocke Tracker

A free GitHub Pages version of the Dandy's World Nuzlocke Tracker,
migrated from Netlify. It is a single self-contained page: runs are saved
in your browser's localStorage, and you can Export / Import a run in the
app to back it up or move it between devices.

## Editing the site

Everything lives in `index.html`. On GitHub you can edit it in the
browser: open `index.html`, click the pencil (Edit) icon, make your
change, and choose "Commit changes". GitHub Pages will redeploy
automatically within a minute or two.

Useful places inside the file:

- Page text and layout: the HTML inside `<body>`, before the `dw-data` script.
- Toons & trinkets: search for `id="dw-data"` — a JSON list with each
  item's name, categories, and embedded image.
- Colors and styling: the `<style>` block in `<head>`.
- Challenges, rewards, and the spin wheel: the final `<script>` —
  search `REWARDS`, `TEAM_TIERS`, or `SPIN_KINDS`.

Tip: keep a backup copy before big edits — an invalid change to the
JSON data block can stop the page loading, and you can always restore
the previous version from the repo's commit history.
