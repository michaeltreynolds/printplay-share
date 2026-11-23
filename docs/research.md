# Research notes (11/23/2026)

## Does this already exist?

Partly, but as separate pieces. I found no site that combines sharing a game's files with sending an order
straight to a print shop.

- **Places to share files:** The Game Crafter (it can sell a print-and-play download), itch.io, BoardGameGeek's file
  section, PnPArcade and DriveThruCards. These files are usually PDFs meant for a home printer, and they often
  need editing before a print-on-demand shop will take them.
- **Printers that make a single copy:** The Game Crafter and MakePlayingCards make single copies, including punch-out tokens.
  Game Crafter's punchouts are 60 pt (about 0.07") chipboard.
- **Factory printers:** PrintNinja and QIN Printing die-cut 1 to 2 mm greyboard, but the minimums are around 500 copies.

**The missing piece:** a list of components plus art that can be shared and adapted, and that turns into an
efficient, easy-to-cut, print-ready PDF and order sheet for one particular vendor.

## FedEx Office

- **Paper:** the heaviest cover stocks are 110 lb (14 pt) and 130 lb (16 pt), gloss on both sides. A 240 lb stock is
  offered only for business cards. 16 pt is fine for cards.
- **Tokens:** real punchboard is about 60 to 80 pt, so FedEx can't print tokens at that thickness. Options:
  1. Print on sticker paper or cardstock and glue it to 2 mm greyboard, then cut (classic print-and-play).
  2. Send only the token sheet to a one-off punchout printer (The Game Crafter or MakePlayingCards).
  3. Use FedEx foam-board mounting for a game board only. It's too thick for tokens.
- **API:** FedEx advertises a Print API, but onboarding goes through sales (onlineprintapi@fedex.com), and one
  developer page says the older Office Web Services are closed to new developers. Plan: the user uploads the PDF
  and follows the order sheet. Sending orders automatically is a stretch goal.

## Easy-to-cut layout

- Butt cards edge to edge so neighbors share cut lines: 9 poker cards (2.5x3.5) per 8.5x11 page with 8 straight
  cuts, and more per sheet on 12x18 or 13x19.
- Add bleed past the cut lines and cut marks in the margin. Double-sided sheets need the back flipped
  (mirrored) so it lines up when printed duplex.
- This is a guillotine cutting-stock / 2D bin-packing problem. Square tokens pack with almost no waste; round
  tokens waste the corners.

## Licensing

Focus: people sharing games they designed themselves, non-commercially. 3D-model sites have each creator choose a
Creative Commons license per model, then enforce adapt and credit rules. PrintPlay Share copies that model
(see the licensing table in the initial design).

HOAX (Eon 1981; Fantasy Flight reprint around 2015 to 2016) is still under copyright. Game mechanics generally
can't be copyrighted, but art and rules text can. So the example project uses **original art and wording**.
The platform needs a license field on every game, a link to the game it was adapted from, and a way to report
content, the same way 3D-model sites do.
