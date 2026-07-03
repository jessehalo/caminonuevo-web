# Camino Nuevo — Design Tokens

Canonical source of truth for the site's visual system. If the HTML `:root`
block or the project instructions statement ever disagree with this file, **this
file wins** — update the others to match.

These values live inline as CSS custom properties in `index.html` (`:root`).
This file is documentation: it records what each value *means* so the design can
be extended later without guessing.

---

## Color

| Token | Hex | Role |
|-------|-----|------|
| `--bg` | `#0A0512` | Midnight indigo. Page background, the base everything sits on. |
| `--magenta` | `#FF2E93` | Primary neon. Headline glow, brightest accent. |
| `--aqua` | `#2FF3E0` | Cool accent. Eyebrow labels, scroll cue, path gradient tail. |
| `--violet` | `#8B5CFF` | Mid accent. Bridges magenta and aqua in gradients. |
| `--amber` | `#FFC15E` | Warm accent — the "sunrise." Used sparingly against the cool field. |

**Gradient logic:** the headline and the SVG path run magenta → violet → aqua
(warm to cool). Amber is the deliberate outlier — one warm note so the palette
doesn't read as a single cool wash. Keep amber rare; it loses meaning if spread.

**Aurora background:** four blurred blobs (magenta, violet, aqua, amber) drifting
over `--bg`, low opacity, blended. That's the festival atmosphere. Don't raise
opacity to the point the text loses contrast.

---

## Type

| Role | Typeface | Notes |
|------|----------|-------|
| Display | **Syne** (700 / 800) | Sculptural, wide, art-collective feel. Hero headline, ethos line, marquee. Used big and with restraint. |
| Body | **Space Grotesk** (400 / 500) | Clean, geometric. All running text, eyebrows, footer. |

Loaded from Google Fonts. The neon-bloom treatment on the display type (gradient
fill + soft text-shadow) is what makes the pairing memorable — the fonts alone
are a neutral pair, the glow is the signature.

---

## Feel (non-negotiable)

Modern festival / neon / new-age. Aurora mesh, fine grain overlay, neon-bloom
headline, and the self-drawing SVG "camino" path as the signature element.
Vague and mysterious by intent — no named destinations, no hard sell.

Accessibility floor: respects `prefers-reduced-motion`, responsive to mobile,
visible keyboard focus. Don't ship changes that break these.

---

## Held for later — the three platforms

If/when the platforms section returns (Sendero / Aurora / Umbral), each card
took its own neon accent from the palette above:

- **Sendero** — `--magenta` — "the trailhead: where the wandering begins"
- **Aurora** — `--amber` — "the first light"
- **Umbral** — `--aqua` — "the threshold: the doorway between who you were and who you're becoming"

Section framing: **"different doors, same horizon."** Cards were glassmorphic
(frosted, low-opacity fill, neon edge glow on hover). The block was removed
cleanly, so bringing it back is a rebuild against these tokens, not a retrofit.
