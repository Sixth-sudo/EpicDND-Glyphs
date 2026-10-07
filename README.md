# EpicDND Glyphs

Damage-type / defense icon SVGs for the **Epic 2024** Roll20 character sheet
([Sixth-sudo/EpicDND](https://github.com/Sixth-sudo/EpicDND)). They live in
this small public repo so Roll20 can hot-link them — chat cards and sheet CSS
can only show images served from a public https URL.

| Folder | Contents |
|---|---|
| `damage-element/` | the 13 damage types plus healing and temp HP, element-coloured |
| `damage-draconic/` | the same 15 in each type's dragon colour (metallic dragons for the physical and healing types) |
| `hidden-elements/` | homebrew secrets (chaos, chromatic, hellfire, physical, sanctified cold, seismic, as-weapon) |
| `defense-markers/` | resistance / immunity / vulnerability shields |
| `conditions/` | condition badges for the Defenses tile (the conditions plus exhaustion, magical sleep, disease and magic), each a silhouette on a dark disc inside a ring of the condition's colour |
| `png/…` | 72px PNG renders of everything above — Roll20's chat image proxy refuses SVG, so chat cards use these |

Open `_contact-sheet.html` in a browser to preview the damage set, and
`_conditions.html` for the condition badges.

## How the sheet uses this repo

The sheet is stamped with this base URL (uncached, correct MIME types for
both the SVGs and the PNGs):

```
https://raw.githubusercontent.com/Sixth-sudo/EpicDND-Glyphs/main
```

In-sheet CSS icons load `<base>/<set>/<key>.svg`; chat cards load
`<base>/png/<set>/<key>.png`.

To re-point or refresh the sheet after changing icons here, run in the main
EpicDND repo:

```
python build-glyphs.py https://raw.githubusercontent.com/Sixth-sudo/EpicDND-Glyphs/main
```

then re-upload `sheet.css` and re-paste `Epic-mod.js` into Roll20.

The source of truth for these files is the `roll20-glyphs/` folder in the main
EpicDND repo — edit there and re-copy, don't let the two drift. The SVGs are
drawn by `build-damage-glyphs.py` (the condition badges by
`build-condition-glyphs.py`) and the PNGs rendered by
`render-glyph-pngs.js`, both in that repo. The filenames are the contract the
sheet relies on, so a redraw is just a re-copy here: the sheet needs no
re-upload.
