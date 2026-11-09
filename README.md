# Dr.Sedeeq Khataat — Arabic calligraphic glyph-forms prototype

A static GitHub Pages prototype that **displays real glyph outlines and their contextual alternates** from the freely licensed Amiri font (SIL OFL 1.1). It is NOT the source code, fonts, or glyphs of Kelk 2010, and it is NOT a Thuluth rules engine.

## Contents
- `index.html`, `style.css`, `app.js`: browser interface
- `glyphs.json`: recorded SVG path outlines, indexed by Arabic letter and positional form, including alternate glyph names
- `fonts/Amiri-Regular.ttf` and `fonts/OFL.txt`: original open-license Amiri font and license

## Usage
Upload **all files and folders** to a public GitHub repository. Enable Settings → Pages → Deploy from branch → main / root. Open the generated website; select `ج`, filter `أول الكلمة`, and inspect its alternate contours. Type `جم` to see a browser-shaped word via Amiri's native OpenType shaping.

> WARNING: alternate glyph names are not a complete set of linguistic/orthographic rules. The gallery inventories possible contours but **does not** automatically determine which variant is lawful in `جم` or other contexts. Browser shaping uses native GSUB/GPOS features; the chosen gallery variant is not substituted into the sample word.

## Next development milestone
Implement an explicit rule database specifying per-alternate: predecessor/successor, allowed joins, baseline posture, stacking relation, style, anchors, substitution priority; implement rule evaluation and collision tests, then manual glyph placement + ligature composition. For a Thuluth system, licensed Thuluth contour sources and calligrapher-validated rules are still needed.

## License
The Amiri font is licensed under SIL OFL 1.1; see `fonts/OFL.txt`. Application source code is original demonstration code; no Kelk resources are included.
