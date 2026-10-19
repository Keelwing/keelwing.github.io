# The Keelwing brand

## The idea

A sailing boat has three layers, and so does Keelwing: what you see and touch is up in the **air** (the sail),
the modules you ride glide on the **surface** (the hull), and what keeps it all steady works in the **depth** (the
keel). The name says the same: a keel below, a wing above. A wing keel is also a real keel, with small wings at its
foot; the mark draws one.

| Layer | In the mark | Colour | Projects |
|---|---|---|---|
| Air: UI and UX | the sail | Air `#14A39A` | Seaglass |
| Surface: modules that glide | the hull | Surface `#3D8BFF` | Sailyard |
| Depth: under the water | the keel | Depth `#0E1B2A` | the runtime, tools to come |

## The mark

A sailing boat from the side, cut by the waterline. Two cuts of it, in `site/brand/`:

| File | Use |
|---|---|
| `keelwing-mark.svg`, `keelwing-mark-dark.svg` | the full mark, from 64 px up; `-dark` for dark grounds |
| `keelwing-mark-compact.svg`, `keelwing-mark-compact-dark.svg` | 48 px and below: a thicker waterline and a plain fin |
| `keelwing-avatar.svg`, `keelwing-avatar.png` | the organization avatar, 500 × 500: the emblem |

On a dark ground the waterline and the keel turn Foam; the sail and the hull keep their colours. Keep clear space
around the mark of at least the hull's height. Don't stretch it, recolour a layer, or add outlines and shadows.

## The emblem

The mark in its own scene, for the avatar and other large places: the boat at dusk, the sun going down behind
it, a small school of fish under the water. The sail and the hull sit in the air, the keel under the water, so the
three layers are there to see. The sky (`#20325F` → `#7C6E9E` → `#F4B98C`), the sun (`#FFD9A0`) and the sea
(`#3A6FB8` → `#173F7E` → `#091A33`) belong to the emblem only. Below 64 px, and wherever a plain mark fits better,
use the mark.

## Colours

| Name | Hex | Use |
|---|---|---|
| Air | `#14A39A` | the sail; the UI layer |
| Surface | `#3D8BFF` | the hull; the gliding layer |
| Depth | `#0E1B2A` | the keel, the waterline, text |
| Night | `#0A1522` | dark grounds |
| Foam | `#EEF3F8` | light grounds, cards; the mark's depth on dark grounds |
| Air text | `#0F6E63` | teal text on light grounds |
| Surface text | `#1D5FD1` | blue text and links on light grounds |
| Line | `#D3DEEA` | borders |
| Muted | `#C3CFDB` | the inactive layers in a layer mark |

Air and Surface are graphic colours: for text on a light ground use Air text and Surface text, which pass 4.5:1.

## Type

- The wordmark: lowercase `keelwing` in Archivo 700, width 112%, tracking −2%.
- Repository names, code and labels: IBM Plex Mono 500.
- Both are under the SIL Open Font License; the site will serve its own copies instead of loading them from a
  font service.

## Layer marks

A project's repositories can carry the mark with only their layer in colour and the other two in Muted; the
waterline always stays. The full mark, with all three layers, belongs to the organization.

## Projects keep their own identity

Seaglass and Sailyard have their own icons and names. Their main colours sit in their layers already: Seaglass's
teal is Air, Sailyard's azure is Surface. Next to a project, the Keelwing mark says where it comes from, never more.

Sailfish OS and Jolla are trademarks of their owners: don't put their logos next to the mark in a way that suggests
they made or endorse Keelwing.
