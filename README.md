# EpicDND Glyphs

Damage-type / defense icon SVGs for the **Epic 2024** Roll20 character sheet
([Sixth-sudo/EpicDND](https://github.com/Sixth-sudo/EpicDND)). They live in
this small public repo so Roll20 can hot-link them — chat cards and sheet CSS
can only show images served from a public https URL.

| Folder | Contents |
|---|---|
| `damage-element/` | the 13 damage types, element-coloured |
| `damage-draconic/` | the same 13 in gem/chromatic dragon hues |
| `hidden-elements/` | homebrew secrets (hellfire, chromatic, chaos, physical, as-weapon) |
| `defense-markers/` | resistance / immunity / vulnerability shields |
| `png/…` | 72px PNG renders of everything above — Roll20's chat image proxy refuses SVG, so chat cards use these |

Open `_contact-sheet.html` in a browser to preview the full set.

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
EpicDND repo — edit there and re-copy, don't let the two drift.
