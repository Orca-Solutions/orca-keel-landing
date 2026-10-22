# Orca · Brand Kit

Draft 0.5, October 22, 2026 (0.4 and 0.3 earlier that day, 0.2 on October 21; 0.4 added the sea, B-13 and B-14; 0.5 makes Depth Keel's color, adds the keel line and the Shallows seal, B-15). Built from the brand brief (`../01-brand-brief.md`) and the Orca Solutions **Signal v1.0** identity package (September 27, 2026), kept in the Orca Keel plan set (not in this repository). Harbor is the default theme; its neutrals are the studio's Ink #171A18 and Chalk #F0EEE7.

The head is vector geometry from Signal's `geometry.json`: the primary cut for 32 px and up, and a micro cut (larger patch, softer dorsal) for 16 to 31 px and favicons. Signal's own usage rules in `source/orca-signal-v1/README.md` apply to the studio's lockup; the rules below apply to the products.

## What is in the kit

```
kit/
├── README.md                     this file
├── mark-usage-sheet.png          clear space, minimum size, one color, the seal, never
├── color-and-type-sheet.png      Harbor and Workshop swatches, the two typefaces
├── sea-sheet.png                 how Depth and Shallows were chosen (the page-ground use shown there was since dropped)
├── depth-sheet.png               the keel line, the Depth lockup, the Shallows seal, the Keel icon, where the sea goes now
├── voice-sheet.md                six rules, we say / never say, sample copy, tone by surface
├── mark/
│   ├── orca-head-ink.svg         the mark in Ink #171A18 (also -chalk, -depth, -shallows, -black, -white)
│   ├── orca-head-micro-ink.svg   the micro cut for 16 to 31 px (same set of colors)
│   ├── orca-head-{ink,chalk,depth,shallows}-{256,512,1024}.png   transparent PNGs
│   └── orca-app-icon-{depth,shallows,ink,chalk}-{180,512,1024}.png   the Keel icon: head on Depth (default), Shallows alternate; ink/chalk kept
├── lockups/                      SVG with text as outlines, and @2x PNG, each in -depth (light grounds), -shallows (dark grounds), -ink and -chalk (one-color print)
│   ├── orca-wordmark             "orca" alone, lowercase
│   ├── orca-lockup               head + orca
│   ├── orca-keel-lockup          head + orca keel, one line: orca 600, keel 400, 0.16 em between
│   ├── orca-keel-stacked         head above orca / keel at equal size: the secondary lockup for narrow spots
│   ├── keel-wordmark             "keel" alone (settings icon source)
│   ├── by-orca                   the endorsement line for Daybook and partner surfaces
│   ├── orca-solutions-words      the studio in words, for product surfaces; the studio's own lockup is in source/
│   ├── *-on-shallows, *-on-depth, *-on-ink   orca-keel, orca-keel-stacked and orca with the ground and clear space built in: Depth on Shallows, Shallows on Depth and on Ink
│   ├── *-titlecase               the title-case set ("Orca Keel"), kept as an alternate, not for new work
│   └── contact-sheet.png         all of the above on Chalk and on Ink
├── scenes/                       the box drawn until there is photography, seal in Shallows: box-on-depth (the product shot), box-on-paper, box-on-shallows, each with and without the lockup, 1600×900 and @2x, plus box.css
└── tokens/
    ├── tokens.json               colors, type scale, space, radius, mark rules, the light
    └── colors.css                the same as CSS custom properties, with a workshop theme and .orca-dark
```

## The rules in brief

**The mark.** Clear space of half the head's height on every side (Signal's own rule is a quarter; the products give it more). Minimum 8 mm in print, 24 px on screen with the primary cut, 16 px with the micro cut. One color only, from four: Ink or Depth on light grounds, Chalk or Shallows on dark. Never Harbor, never two colors. The eye is a hole that shows the ground. It faces right. Never inside a circle, plate or badge; never rotated, stretched, outlined, shadowed or gradient-filled; never next to the old rounded lowercase "orca." One exception, the icon form (B-15): the head in Paper on a Depth rounded square (radius 23.4% of the side, `orca-app-icon-depth-*`) is allowed only where an icon is called for: the site's header tile, the favicon, the app icon. Never on the box, the carton or paper.

**The seal.** The head alone is pressed into every physical product: debossed in the box's top surface and inlaid in Shallows (about 18 mm, beside the amber light; jason, 2026-10-22: a black body with a pale patch is what an orca is); blind-embossed in the carton board, no ink; printed in Depth on the card. No word with it.

**Lockups.** Lowercase, like the studio's lettering (jason, 2026-10-22). Color: Depth on light grounds, Shallows on dark grounds (Depth, Ink); Ink and Chalk for one-color print. The umbrella on product surfaces is the head plus "orca" in Instrument Sans semibold. A product is "orca" semibold followed by its word in regular at the same size, 0.16 em apart, never a full space: orca keel. In running text the name is written Orca Keel; lowercase is for the lockup only. Two structures, two owners: inline and same-size is the product's primary; the same-size stack (`orca-keel-stacked`) is the product's secondary for narrow spots such as a box side or a square icon context; the big-word/small-word stack (big "orca", small spaced word beneath) is the studio's alone, because "solutions" is descriptive and a product's second word is the point. The studio keeps its Signal lockup (head + lowercase orca / solutions in outlined Helvetica Neue) on its own site and documents; on product surfaces it is "Orca Solutions" in words at a smaller size. Software (Daybook) keeps its own name and icon and carries "by Orca" where there is room.

**Color.** The family rule (jason, 2026-10-22, B-14; "the wheelhouse has many spokes, but it must be an integrated whole too"): every Orca product shares the two-tone, Ink and Chalk, and carries its own accents; the studio has Vermilion, Garnet Guard its garnet, Diamond Dog its green and purple, and Orca Keel the sea. On Keel: Paper ground, Ink text, Stone for secondary text, Linen for rules; the sea at three depths as the accent (Shallows, Harbor, Depth), with Harbor the only one that is ever text; Amber as the one warm point of contrast. The installer's layer is Ink ground with Paper text (`.orca-dark`).

**The sea** (jason, 2026-10-22, B-13 and B-15). One hue at three depths. Depth #11404B is Keel's color: the keel line (3 px at the top of every Keel surface: page header, card, carton; `.keel-line`), the lockup and the head on light grounds, the primary action (`.button`), a dark band for the hero and the product shot the way Ink is the installer's band (`.orca-depth`), the Keel icon, covers, and the carton's one ink. Shallows #D8E6E4 is the sea's light: the lockup and text on dark grounds, the seal inlaid in the box, small panels (`.orca-panel`). It is never a page ground or a wash (jason). Harbor #1E5A66 is for links and selected states on light grounds, and a band only where Depth would be too heavy. Never: Depth or Shallows as body text on light grounds, the box's finish, the light, gradients, photographs of water.

**The one point** (B-14). Amber is the true contrast to the sea, and it stays rare so it keeps its meaning. On the box it is the listening light. In the app it marks the listening state and nothing else. On the site and in print it may appear once per page as a point, never an area: the period that ends a headline, the arrow on a link, the way the studio's site uses its Vermilion. Never text, never a fill, never a button, never on the mark. No fourth color: a warm red would blur into the studio's Vermilion, and Amber already sits opposite the sea on the wheel.

**Type.** Instrument Sans is the product's voice (wordmark, interface, headings, carton). Newsreader is the record's voice (Daybook entries, matters, long copy). No third face; monospace only in installer documentation.

**The light.** Off when idle. Amber and steady while listening. One blink on power. It is the only lit element on the hardware.

## Using the tokens

```html
<link href="https://fonts.googleapis.com/css2?family=Instrument+Sans:wght@400;500;600&family=Newsreader:ital,opsz,wght@0,6..72,400;0,6..72,500;1,6..72,400&display=swap" rel="stylesheet">
<link rel="stylesheet" href="tokens/colors.css">
```

Add `data-theme="workshop"` to `<html>` for the alternative palette. Use `.orca-dark` on a section for the installer's layer.

## Rebuilding the exports

The SVG lockups set text as outlines from the Google Fonts TTFs (Instrument Sans 400/500/600) so they render identically everywhere. The PNGs were rendered with headless Chromium at 2x. The inputs are Signal's `geometry.json` and the fonts; the studio's own `source/build.py` and `export.mjs` rebuild the studio lockups.

## What is still placeholder

- Photography: none yet. The box drawn as a dark slab with the Shallows seal, on Depth or Paper (`scenes/`), stands in.
- Prices, dates, unit counts, the app link and the pairing code on the card: bracketed placeholders until the pilot.
- The carton dieline and the card at print size: mocked on the canvas, not yet drawn to dimensions.
