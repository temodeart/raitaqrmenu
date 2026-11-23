# Lighthouse — QR table menu

Mobile-first digital menu for Lighthouse cafe & bar (@raita_lighthouse), opened by scanning the QR code on each table.

Live: https://temodeart.github.io/raitaqrmenu/

## Editing the menu
All items and prices live in the `MENU` array near the top of the `<script>` in `index.html`.
- Prices are in thousands of ₮: `30` shows as "30k".
- Spirits use `[50ml, bottle]`; `null` shows "—".
- Order changes with the time of day (Ulaanbaatar time): 06:00–16:59 food, coffee and soft drinks come first; from 17:00 cocktails, beer, wine and spirits come first (`DAY_ORDER` / `NIGHT_ORDER`).
- Lunch: weekdays 12:00–14:00 (`SERVE_FROM` / `SERVE_TO`). It sits at the front from 06:00 until 14:00 on weekdays and glows while it's being served; otherwise it goes last.

Push to `main` and GitHub Pages updates the live page within a minute or two. The QR code points at the live URL, so it never needs reprinting.

## Print
`print/` holds the QR code and the table cards:
- `lighthouse-table-card-A6-bleed.pdf`: A6 card (105 × 148 mm) with 3 mm bleed, for a print shop.
- `lighthouse-table-card-A6.pdf`: same card at trim size, no bleed.
- `lighthouse-table-cards-A4-4up.pdf`: four cards on one A4 sheet with dashed cut lines, for printing in-house.
- `qr-menu.svg` / `qr-menu.png` / `qr-menu-black.svg`: the QR code on its own.
- `card.html`: source for the cards (render with a browser's print to PDF).
