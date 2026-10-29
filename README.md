# OSCA Nature Travel for Safari – Website

A simple one-page website using only HTML, CSS and JavaScript. No installation, database or paid service is needed.

## What is in this folder
| File | Purpose |
|---|---|
| index.html | The page content (text, packages, destinations) |
| styles.css | Colors, layout and mobile design |
| script.js | WhatsApp booking buttons and mobile menu |
| images/ | Pictures (see images/README.md) |

## Before you publish: 3 things to edit
1. **WhatsApp number** – open `script.js`, find `REPLACE_WITH_WHATSAPP_NUMBER` and replace it with the real number in international format, digits only, no plus sign (example format: `2557XXXXXXXX`). Keep the quote marks.
2. **Contact details** – in `index.html`, search for `[Add` and replace each bracketed placeholder.
3. **Prices and inclusions** – the four package prices are **sample prices, not confirmed**. Edit them in `index.html` (search for `Sample Price`) once the company confirms real rates, and fill in the "What's Included / Excluded" text.

## Test on your computer
Double-click `index.html` to open it in your browser. Everything works except actual WhatsApp messages, which need a real number.

## Deploy with GitHub and Cloudflare Pages (free)
**A. Put the files on GitHub**
1. Create a free account at github.com and click **New repository**. Name it, for example, `osca-safari`.
2. Click **uploading an existing file**, then drag in the **contents** of this folder (index.html, styles.css, script.js, README.md and the images folder). `index.html` must be at the top level of the repository.
3. Click **Commit changes**.

**B. Publish with Cloudflare Pages**
1. Create a free account at cloudflare.com and open **Workers & Pages**.
2. Choose **Create application**, then the **Pages** option, then **Connect to Git**, and pick your `osca-safari` repository.
3. Settings: **Framework preset** = None, **Build command** = leave empty, **Build output directory** = `/` (or leave empty).
4. Click **Save and Deploy**. After a minute you get a free `.pages.dev` web address.

**C. Update the site later**
Edit a file on GitHub (pencil icon) or upload a new version, then **Commit changes**. Cloudflare republishes automatically.

## How to edit common things
- **Text:** edit `index.html` between the tags.
- **Colors:** edit the values at the top of `styles.css` under `:root`.
- **Add a package:** copy one whole `<article class="package-card"> ... </article>` block in `index.html`, paste it after the last one, then change its text and its `data-package="..."` name.
- **Images:** see `images/README.md`.

## Notes
- Pressing a "Book This Safari" button only opens WhatsApp with a prefilled message. Nothing is booked until the visitor sends it and the company replies.
- The page loads two free Google Fonts. If they cannot load, the site falls back to standard fonts.
