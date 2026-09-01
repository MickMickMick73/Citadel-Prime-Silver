# Citadel Prime Silver

Chrome + royal-blue enamel plates for MixMods / Oxide menus, matched to the **Citadel Prime Silver** supporter crest.

Fan-made UI kit. Not affiliated with Citadel Prime or Facepunch.

## Buttons

720×240 PNG, **no letters** (you overlay CUI / CSS text). Four states each.

| id | look |
| --- | --- |
| `silver` | Polished chrome plate, blue inner glow |
| `royal` | Deep royal enamel, silver bevel |
| `crown` | Chrome with crown notches |
| `keep` | Dark stone keep, merlons |
| `banner` | Royal silk with silver swallowtail |

```
buttons/<id>/normal.png
buttons/<id>/hover.png
buttons/<id>/pressed.png
buttons/<id>/disabled.png
```

Sprite button CSS (same silhouette as MixMods plates):

```css
.rui-sprite {
  background: var(--rui-n) center / 100% 100% no-repeat;
}
.rui-sprite:hover:not(:disabled) { background-image: var(--rui-h); }
.rui-sprite:active:not(:disabled) { background-image: var(--rui-p); }
.rui-sprite:disabled { background-image: var(--rui-d); }
```

## Frames (9-slice)

720×720, hollow centre, 96px slice.

`shield` · `keep` · `crown` · `banner` · `prime`

```html
<div class="mm-frame mm-frame--cit-shield">…</div>
```

```css
.mm-frame {
  border: 48px solid transparent;
  border-image-slice: 96 fill;
  border-image-repeat: stretch;
}
.mm-frame--cit-shield { border-image-source: url("frames/shield.png"); }
```

## Panels (filled halls)

Buttons sit on these, not a hole.

`citadel` · `throne` · `hall`

```html
<div class="mm-panel mm-panel--citadel">
  <button class="rui-sprite">ENTER</button>
</div>
```

Load `citadel-kit.css` from this repo.

## Crest

`crest.png` — reference lockup (not a UI plate).

## Licence

Use on your own servers and menus. Do not sell the crest artwork as your own. Palette and plates are provided as-is.
