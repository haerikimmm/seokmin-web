# Seokmin Park — portfolio

Single-page portfolio for Seokmin Park: metalsmith, digital fabricator, welder. Seoul.

## Stack

Static. One `index.html` with inline CSS and JS, plus optimised images. No build step,
no dependencies, no framework. Any static host will serve it as-is.

- Display type: [VT323](https://fonts.google.com/specimen/VT323) (Google Fonts)
- Body type: [Stack Sans Text](https://fonts.google.com/specimen/Stack+Sans+Text) (Google Fonts)
- Light and dark themes, remembered in `localStorage`, defaulting to the OS setting

## Layout

```
index.html      the whole site
img/            webp, two sizes per photo:
                  <slug>.webp    up to 1600px, used in the plate grids and hover previews
                  <slug>-t.webp  up to 560px, used for thumbnails and hero artifacts
img/manifest.json  source filename and original dimensions for every image
```

Image slugs are prefixed by body of work: `pls-` plaster, `mtl-` interior metal,
`ins-` insulation, `pp-` Precious Plastic, `edu-` fab lab teaching, `sk-` sketches
and personal work.

## Running locally

```bash
python3 -m http.server 4321
```

Then open http://localhost:4321. Opening `index.html` as a `file://` URL also works.

## Adding photos

Source photos are kept outside the repo. To add more, resize to the two sizes above and
write them into `img/` with a matching slug, then reference the slug from the relevant
array in `index.html` (`ART`, `WORK`, `PLATES`, `PLATES_PLS`).

## Notes

Body copy is a working draft and needs Seokmin's review before it is treated as final,
particularly the About section and the claims about plaster technique and Fab City.
