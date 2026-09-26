# GeoSET project page

Source of the project page for **GeoSET: Generalist Foundation Model for SAR-to-EO Image Translation**
(Jeonghyeok Do, Munchurl Kim; KAIST; arXiv preprint, 2026).

- Live page: https://kaist-viclab.github.io/GeoSET_site/
- Code repository: https://github.com/KAIST-VICLab/GeoSET

The page is plain HTML, CSS and JavaScript with no build step and no dependencies other than Google Fonts.
GitHub Pages serves it from the repository root (`.nojekyll` turns off Jekyll processing).

## Preview locally

Serve the folder over HTTP rather than opening `index.html` from disk, so that every path resolves as it does on GitHub Pages:

```bash
cd GeoSET_site
python3 -m http.server 8000
# then open localhost:8000 in a browser
```

## Layout

```
index.html                the page (results first: headline figures, interactive gallery, quantitative results, then a compact method overview)
static/css/family.css     styles shared with the GeoSET, GeoCR and MotionMaestro pages (the same file on all three)
static/js/family.js       scripts shared with those pages: navigation, abstract toggle, pending links, BibTeX copy,
                          image lightbox, tabs, table scroll cues
static/css/style.css      GeoSET brand colours (top of the file) and the gallery, comparison slider, radar and table view toggle
static/js/main.js         interactive gallery (tile strips in carousels), comparison slider, table view toggle
static/images/            figures (web size + *_full.jpg for the lightbox), radar.png, og.jpg (social preview) and the logo files
static/tiles/             per-method image tiles for the interactive gallery
```

## Logo

The GeoSET logo is included: `static/images/logo.svg` is the hero title, `icon.svg` is the navigation and footer mark,
and `icon_square.svg` (the SVG favicon), `favicon-32.png`, `favicon-64.png` and `apple-touch-icon.png` are the browser and
home-screen icons. The page title and headings use the logo's typeface, Outfit (loaded from Google Fonts), and the logo's
colours (ink `#1C2738`, blue `#1B6FCB`).

## arXiv link

The arXiv ID is not assigned yet. Until it is, the Paper and arXiv buttons, the navigation bar's Paper link, the footer's
arXiv link and the BibTeX entry hold a placeholder ID; a link that holds it is shown as pending (the Paper and arXiv buttons
carry a "soon" badge) and does not navigate, with or without JavaScript. The arXiv link will be added once the paper is on arXiv: replacing the placeholder in
`index.html` with the real ID is enough, and the links then work as normal links. No CSS or JavaScript file needs editing.
