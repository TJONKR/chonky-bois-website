# Bongo Cat Website - THE CONCEPT

## The Vision

Clean, minimal Apple-style UI... but the ENTIRE BACKGROUND is a grid of bongo cats.
Every cat reacts to your keyboard/mouse. Type = they all tap. Click = they all bonk.

It's an INVASION of cuteness.

```
+------------------------------------------------------------------+
|  BACKGROUND: GRID OF CATS (always visible, behind everything)     |
|  +----+----+----+----+----+----+----+----+----+----+----+----+    |
|  |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |    |
|  +----+----+----+----+----+----+----+----+----+----+----+----+    |
|  |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |    |
|  +----+----+----+----+----+----+----+----+----+----+----+----+    |
|  |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |    |
|  +----+----+----+----+----+----+----+----+----+----+----+----+    |
|  |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |    |
|  +----+----+----+----+----+----+----+----+----+----+----+----+    |
|  |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |    |
|  +----+----+----+----+----+----+----+----+----+----+----+----+    |
|  |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |cat |    |
|  +----+----+----+----+----+----+----+----+----+----+----+----+    |
|                                                                    |
|  FOREGROUND: Clean glass/frosted panels floating on top            |
|                                                                    |
+------------------------------------------------------------------+
```

## Layout

```
BACKGROUND LAYER (z-index: 0)
=============================
Entire viewport = grid of cat squares
- Each square ~100-150px
- Random mix of all available skins
- ALL cats animate together on keypress/click
- Slight opacity (70-80%) so it doesn't overwhelm
- Maybe subtle parallax on scroll?

FOREGROUND LAYER (z-index: 10)
==============================
Floating glass/frosted cards with the actual content

+------------------------------------------------------------------+
|                                                                    |
|  CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS      |
|  CATS +--------------------------------------------------+ CATS   |
|  CATS |                                                  | CATS   |
|  CATS |     B O N G O  C A T                             | CATS   |
|  CATS |                                                  | CATS   |
|  CATS |     Your menu bar companion that                 | CATS   |
|  CATS |     taps along to your keyboard                  | CATS   |
|  CATS |                                                  | CATS   |
|  CATS |     [  Download for macOS  ]                     | CATS   |
|  CATS |                                                  | CATS   |
|  CATS |     Try it now - type anything!                  | CATS   |
|  CATS |                                                  | CATS   |
|  CATS +--------------------------------------------------+ CATS   |
|  CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS      |
|  CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS      |
|                                                                    |
|  CATS +--------------------------------------------------+ CATS   |
|  CATS |                                                  | CATS   |
|  CATS |  FEATURES                                        | CATS   |
|  CATS |                                                  | CATS   |
|  CATS |  [icon]        [icon]         [icon]             | CATS   |
|  CATS |  30+ Skins     Lightweight    Menu Bar           | CATS   |
|  CATS |                                                  | CATS   |
|  CATS +--------------------------------------------------+ CATS   |
|  CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS CATS      |
|                                                                    |
+------------------------------------------------------------------+
```

## Cat Grid Behavior

```
IDLE STATE:
+--------+--------+--------+--------+
|  idle  |  idle  |  idle  |  idle  |
| (^.^)  | (^.^)  | (^.^)  | (^.^)  |
+--------+--------+--------+--------+

ON KEYPRESS (ripple effect from center):
+--------+--------+--------+--------+
| TAP!   | TAP!   | TAP!   | idle   |  <- wave spreads out
| \(^.^)/| \(^.^)/| \(^.^)/| (^.^)  |
+--------+--------+--------+--------+

ON CLICK (all cats near cursor react):
+--------+--------+--------+--------+
|  idle  | BONK!  | BONK!  |  idle  |
| (^.^)  | \(°o°)/| \(°o°)/| (^.^)  |
+--------+--------+--------+--------+
           ↑ click happened here
```

## Interaction Ideas

1. **Type on keyboard** → All cats do tap animation (wave ripple from center)
2. **Click anywhere** → Nearby cats react with tap_both animation
3. **Hover over a cat** → That cat does a special wiggle
4. **Scroll** → Subtle parallax, cats in background move slower
5. **Easter egg**: Type "meow" → All cats change to a random skin

## Visual Style

### Foreground Cards (Apple-style)
- Frosted glass effect (backdrop-filter: blur)
- Subtle white/cream background with 80% opacity
- Rounded corners (20-24px)
- Soft shadows
- Clean SF Pro or similar typography
- Minimal, lots of whitespace inside cards

### Background Cat Grid
- Slight desaturation or lower opacity (70-80%)
- Each cat randomly assigned a skin on load
- Grid gaps very small (2-4px) or none
- Covers entire viewport, tiles as needed

### Colors
- Background tint: soft warm cream (#FEF7EC) or cool gray (#F4F4F5)
- Card background: white/cream with blur
- Text: Near black (#1A1A1A)
- Accent: Coral (#FF6B6B) or your brand color
- The CATS provide all the color variety!

## Mobile Consideration

- Fewer cats in grid (smaller grid)
- Touch = tap animation
- Cards stack vertically
- Maybe cats only visible behind hero on mobile?
