# Olive Tree Baby & Kids Clinic — website

A static site (plain HTML/CSS/JS) built to replace the Weebly site before it goes dark on
27 September 2026.

## Files

- `index.html`, `about.html`, `services.html`, `contact.html` — the four pages
- `styles.css` — all styling
- `script.js` — mobile nav toggle + scroll animations
- `CNAME` — tells GitHub Pages which custom domain to serve this on
- `favicon.ico` — browser tab icon, generated from the clinic's real logo
- `images/favicon-16.png`, `images/favicon-32.png` — sharper favicon variants for modern browsers
- `images/apple-touch-icon.png` — icon used when someone saves the site to an iPhone home screen

## Publishing on GitHub Pages

1. Create a new GitHub repository (public) and upload all these files to it.
2. In the repo, go to **Settings → Pages**, set the source branch to `main` (root folder).
3. Under **Settings → Pages → Custom domain**, enter `www.olivetreebabykidsclinic.sg`
   (this matches the `CNAME` file already included).
4. At your domain registrar's DNS panel, add:
   - A **CNAME** record: `www` → `<your-github-username>.github.io`
   - (Optional, for the bare domain) four **A** records for `@` pointing to:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
5. Wait for DNS to propagate (up to 24–48h), then tick **Enforce HTTPS** in Pages settings
   once GitHub shows the domain as verified.

## Still to do before launch

- **Photos**: drop image files into an `/images` folder in the repo, named exactly as below.
  Until a file exists at that path, the site shows a dashed placeholder box telling you which
  filename it's waiting for — so nothing looks broken in the meantime.
  - `images/drtan.jpg` — Dr Tan's photo (used on both the homepage hero and About page)
  - `images/drlim.jpg` — Dr Lim's photo (About page)
  - `images/gallery-1.jpg` through `images/gallery-5.jpg` — clinic photos for the homepage
    gallery (waiting area, consultation room, reception, play corner, exterior — rename/add
    more as you like, just keep the `gallery-N.jpg` pattern or update the `src` attributes
    in `index.html` to match whatever filenames you use)
- **Contact form**: currently points to a placeholder Formspree endpoint. Sign up free at
  formspree.io, create a form, and replace `REPLACE_WITH_YOUR_FORMSPREE_ENDPOINT` in
  `contact.html` with your real endpoint — otherwise the form won't send anywhere yet.
- **Fees**: the homepage has a placeholder "Consultation fees" section with dashes where real
  amounts should go — update the `fee-amount` values in `index.html` once you have pricing.
- **Email**: now live throughout the site as `olivetreekidsclinic@gmail.com` — update in
  `index.html`, `contact.html`, and the footer of every page if this changes.
