# Ironvale website

A static website: one `index.html`, two legal pages, a 404 page and the 3D library in `vendor/`.
No build step and no server code. It runs on any static host.

## Files

| File | What it is |
|---|---|
| `index.html` | The full site: 3D ocean story, sectors, crew finder, estimator, booking and join forms, certificate checker, client portal preview |
| `privacy.html`, `terms.html` | Legal page templates. Fill in the highlighted items and have them reviewed before launch |
| `404.html` | Page shown for broken links (most hosts pick it up automatically) |
| `robots.txt`, `sitemap.xml` | For search engines. Replace `yourdomain.com` with your domain |
| `vendor/three.min.js`, `vendor/three.LICENSE` | 3D library and its licence. Keep both |
| `CREDITS.md` | Licences for the library and fonts |

## Before going live

1. **Settings.** Open `index.html`, search for `SITE SETTINGS` and set:
   - `email`: the contact address shown on the page.
   - `formEndpoint`: the URL that should receive booking and join forms. Create a free form on a form service
     (for example Formspree, Getform or Basin) and paste its endpoint URL. While this is empty the forms work in preview mode
     and nothing is sent.
2. **Domain.** Replace `https://www.yourdomain.com` in `index.html` (canonical and og:url), `robots.txt` and `sitemap.xml`.
3. **Legal pages.** Complete every highlighted `[ ]` item in `privacy.html` and `terms.html`.
4. **Brand check.** Before you print or register anything, check that "Ironvale" is free to use as a business name and
   trademark in your country, and that the domain is available.
5. **Sample data.** The crew finder, estimator rates and portal use sample data and are labelled as such.
   When you have real data, the lists are near the top of the main script (`TRADES`, `SECTORS`, `WORKERS`).

## Publishing

Upload the whole folder (keep the structure) to any static host:

- **Netlify:** drag the folder onto app.netlify.com/drop, then add your domain.
- **Vercel:** create a project from the folder, framework preset "Other".
- **Cloudflare Pages, GitHub Pages, or your existing hosting (cPanel / FTP):** upload the files to the web root.

Use HTTPS (all the hosts above provide it free).
