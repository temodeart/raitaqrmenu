# Lighthouse — QR table menu

Mobile-first digital menu for Lighthouse cafe & bar (@raita_lighthouse), opened by scanning the QR code on each table.

Live: https://temodeart.github.io/raitaqrmenu/

## Editing the menu
All items and prices live in the `MENU` array near the top of the `<script>` in `index.html`.
- Prices are in thousands of ₮: `30` shows as "30k".
- Spirits use `[50ml, bottle]`; `null` shows "—".
- Lunch: weekdays 12:00–14:00 (`SERVE_FROM` / `SERVE_TO`). Lunch moves to the front of the filters until 14:00 (`DAY_FROM` / `DAY_TO`) and glows while it's being served.

Push to `main` and GitHub Pages updates the live page within a minute or two. The QR code points at the live URL, so it never needs reprinting.

`print/` holds the QR code and the print-ready table cards.
