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

Open `_contact-sheet.html` in a browser to preview the full set.

## How the sheet uses this repo

The sheet is stamped with this base URL (served by jsDelivr with the correct
`image/svg+xml` MIME type):

```
https://cdn.jsdelivr.net/gh/Sixth-sudo/EpicDND-Glyphs@main
```

To re-point or refresh the sheet after changing icons here, run in the main
EpicDND repo:

```
python build-glyphs.py https://cdn.jsdelivr.net/gh/Sixth-sudo/EpicDND-Glyphs@main
```

then re-upload `sheet.css` and re-paste `Epic-mod.js` into Roll20.

Note: jsDelivr caches `@main` for up to ~12 hours after a push. If you need an
edit to show up immediately, either purge via jsDelivr or use the uncached
GitHub raw base instead:
`https://raw.githubusercontent.com/Sixth-sudo/EpicDND-Glyphs/main`

The source of truth for these files is the `roll20-glyphs/` folder in the main
EpicDND repo — edit there and re-copy, don't let the two drift.
