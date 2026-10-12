# Dandy's World Nuzlocke Tracker

A free GitHub Pages version of the Dandy's World Nuzlocke Tracker,
migrated from Netlify. It is a single self-contained page: runs are saved
in your browser's localStorage, and you can Export / Import a run in the
app to back it up or move it between devices.

## What's in the app

- **Challenge modes you combine yourself** — in the challenge editor,
  tick any combination of One-time goal, Checklist, and Counters.
  There is no "hybrid" type anymore; a counter can simply have a
  checklist attached, and each section on the card can be shown/hidden.
- **X-of-Y completion** — "Complete when ___ conditions are met" lets a
  challenge finish without 100% (e.g. 2 of 3 boxes checked). Each checked
  box and each finished counter counts as one condition. Blank = all.
  When a number is set, the progress bar is measured against that
  number (e.g. 2/3), not the total.
- **Multiple checklists per challenge** — a challenge can hold several
  named checklists (add them in the editor), and each one collapses
  independently on the card.
- **Custom challenge icons** — per challenge: an emoji, any toon or
  trinket sprite, or your own uploaded image (shrunk automatically).
- **Team-goal rarity tabs** — All / Bronze / Silver / Gold / Iridescent.
- **Friends tab** — two ways to follow other people's progress:
  a *live group* (create one or join with a group code — progress then
  syncs in real time through a free Supabase project; the group code
  is the group's shared password), and *snapshots* (import a friend's
  share code to see their progress as of that moment). Opening any
  friend shows their specific toons and trinkets by name and sprite,
  not just counts.
- **Drag to reorder** — drag challenges by the ⠿ handle (works with
  touch) instead of clicking the arrow buttons over and over. The
  arrows still work too.

Old saves and old share codes load as before — previous challenge types
are converted to the new mode combinations automatically.

## Editing the site files

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
