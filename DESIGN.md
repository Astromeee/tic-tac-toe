---
name: Arcade Break
description: A pocket-sized retro arcade for quick games between classes.
colors:
  midnight-cabinet: "#080D25"
  indigo-panel: "#111B43"
  indigo-raised: "#192755"
  pixel-lime: "#B9F227"
  coin-amber: "#FFAA19"
  screen-blue: "#62D9FF"
  cloud-white: "#F5F7FF"
  muted-blue: "#B8C4EA"
  cabinet-line: "#405385"
typography:
  display:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "2rem"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: "-0.03em"
  body:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 500
    lineHeight: 1.5
  label:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.78rem"
    fontWeight: 800
    lineHeight: 1.2
    letterSpacing: "0.04em"
rounded:
  sm: "4px"
  md: "8px"
  lg: "14px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
components:
  button-primary:
    backgroundColor: "{colors.pixel-lime}"
    textColor: "{colors.midnight-cabinet}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "12px 16px"
  game-panel:
    backgroundColor: "{colors.indigo-panel}"
    textColor: "{colors.cloud-white}"
    rounded: "{rounded.lg}"
    padding: "24px"
---

# Design System: Arcade Break

## 1. Overview

**Creative North Star: "The Pocket Cabinet"**

Arcade Break borrows the crisp geometry, saturated indicator colors, and tactile controls of a beloved handheld console. It feels playful and energetic while keeping the active game more prominent than its decoration.

Pixel styling is reserved for the wordmark, player marks, scores, and small accents. Standard sans-serif text protects readability. The system rejects neon overload, illegible pixel typography, decorative glassmorphism, generic SaaS cards, and motion that delays play.

**Key Characteristics:** compact, tactile, high-contrast, expandable, responsive.

## 2. Colors

Deep indigo creates the cabinet; lime, amber, and sky blue communicate selection and game state.

### Primary
- **Pixel Lime** (`#B9F227`): active navigation, primary actions, and Player X.

### Secondary
- **Coin Amber** (`#FFAA19`): Player O and celebratory accents.
- **Screen Blue** (`#62D9FF`): focus, informational state, and supporting accents.

### Neutral
- **Midnight Cabinet** (`#080D25`): page background.
- **Indigo Panel** (`#111B43`): main surfaces.
- **Cloud White** (`#F5F7FF`): primary text.
- **Muted Blue** (`#B8C4EA`): secondary text.
- **Cabinet Line** (`#405385`): borders and inactive controls.

**The Three-Light Rule.** Lime selects, amber distinguishes Player O, and blue focuses or informs. Do not interchange their semantic roles.

## 3. Typography

**Display Font:** system monospace stack
**Body Font:** system sans-serif stack
**Label/Mono Font:** system monospace stack

**Character:** Arcade flavor appears in compact, heavy monospace headings. Body copy stays clean and familiar.

### Hierarchy
- **Display** (900, `2rem`, 1): wordmark and major game title only.
- **Title** (850, `1.15rem`, 1.2): panel headings and status.
- **Body** (500, `1rem`, 1.5): instructions, capped at 70 characters.
- **Label** (800, `0.78rem`, 0.04em): controls and compact metadata.

**The Readable Pixel Rule.** Never use the monospace display treatment for paragraphs or small helper text.

## 4. Elevation

Depth is structural: stacked indigo tones, crisp borders, and short offset shadows make controls feel pressable. Wide ambient shadows and glass blur are not part of the system.

### Shadow Vocabulary
- **Tactile control** (`box-shadow: 0 4px 0 #050817`): buttons and selectable game tabs.
- **Active screen** (`box-shadow: 0 0 0 2px #62D9FF`): focus and selected board feedback.

**The Pressed-State Rule.** Interactive shadows collapse on active press so the surface moves toward the cabinet.

## 5. Components

### Buttons
- **Shape:** compact corners (`4px` to `8px`) with a short offset shadow.
- **Primary:** Pixel Lime with Midnight Cabinet text and at least a 44px height.
- **Hover / Focus:** brighten the border; use a 3px Screen Blue focus ring.
- **Secondary:** Indigo Raised with Cloud White text and Cabinet Line border.

### Cards / Containers
- **Corner Style:** restrained (`14px` maximum).
- **Background:** Indigo Panel or Indigo Raised.
- **Shadow Strategy:** no ambient card shadow; use borders and tonal separation.
- **Internal Padding:** `16px` on mobile, `24px` on larger screens.

### Navigation
- The game switcher uses one selected tab and disabled upcoming-game controls. On small screens it becomes a horizontally scrollable row without hiding labels.

### Game Cell
- A square Indigo Raised button with a clear empty hover state. X uses lime plus crossed strokes; O uses amber plus a ring, so neither mark depends only on color.

## 6. Do's and Don'ts

### Do:
- **Do** keep every interactive target at least `44px` square.
- **Do** reserve Pixel Lime for the current game, primary action, and Player X.
- **Do** preserve visible labels alongside decorative pixel icons.
- **Do** provide reduced-motion alternatives and persistent keyboard focus.

### Don't:
- **Don't** use neon overload or glow every inactive surface.
- **Don't** use illegible pixel typography for body copy.
- **Don't** use decorative glassmorphism or generic SaaS card grids.
- **Don't** add motion that delays play.
- **Don't** use color as the only way to distinguish X, O, focus, or winning cells.
