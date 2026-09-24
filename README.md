# CPbOX

CPbOX is a simple, responsive Bengali-first static website for organized app information and official download sources.

## Structure

- `index.html` — SEO-friendly home page
- `pages/` — individual content pages
- `assets/css/` — site styles
- `assets/js/` — site JavaScript
- `assets/manifest.webmanifest` — web app metadata
- `robots.txt` and `sitemap.xml` — crawler guidance

## SEO notes

The site includes semantic headings, descriptive page titles, meta descriptions, canonical URLs, internal links, mobile-responsive CSS, and a sitemap. These improve crawlability and usability, but no website can guarantee a Google ranking; useful original content, reliable links, page speed, and Search Console submission are also important.

## Local preview

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000/`.
