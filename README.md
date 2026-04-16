# Mirmic Company Site

Single-page brochure site for **Mirmic** — a parent brand for consumer software products. Currently hosts the landing page linking to ZzzCam.

## Files

- `index.html` — the page
- `style.css` — dark theme with subtle radial gradients and a soft blue accent
- `favicon.svg` — logo mark (ring + center dot)

Pure HTML + CSS. No build step.

## Publishing to GitHub Pages

1. Move this folder somewhere outside the KidsNightCam repo (e.g. `~/mirmic-site/`).
2. Create a new **private** GitHub repo — suggested name `mirmic` or `mirmic-site` under the `asterisksf` account.
3. Initialize and push:
   ```bash
   cd ~/mirmic-site
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/asterisksf/mirmic.git
   git push -u origin main
   ```
4. In the new repo's GitHub settings → **Pages** → Source: "Deploy from a branch" → Branch: `main`, Folder: `/` (root). Save.
5. After a minute, the site will be live at `https://asterisksf.github.io/mirmic/`.
6. Point `mirmic.co` to it:
   - In GitHub repo settings → Pages → **Custom domain**: `mirmic.co`
   - At your domain registrar (wherever you bought `mirmic.co`), set these DNS records:
     - **A records** for the apex (`mirmic.co`) pointing to GitHub's IPs:
       - `185.199.108.153`
       - `185.199.109.153`
       - `185.199.110.153`
       - `185.199.111.153`
     - **CNAME** for `www.mirmic.co` → `asterisksf.github.io.`
   - Wait for DNS propagation (5 min to a few hours), then enable "Enforce HTTPS" in GitHub Pages settings.

## Customizing

- **Accent color**: change `--accent` in `style.css`
- **Product cards**: duplicate the `.product-card` block in `index.html` for future products
- **Copy**: the manifesto and values sections are editable in `index.html`
