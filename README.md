# Olive Tree Baby & Kids Clinic — website

A static site (plain HTML/CSS/JS) built to replace the Weebly site before it goes dark on
27 September 2026.

## Files

- `index.html`, `about.html`, `services.html`, `contact.html` — the four pages
- `styles.css` — all styling
- `script.js` — mobile nav toggle + scroll animations
- `CNAME` — tells GitHub Pages which custom domain to serve this on

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

- **Photos**: none are hotlinked from the old Weebly site (those links will break when Weebly
  shuts down), so the design currently uses illustration only. Save your real photos from the
  Weebly site now (Settings → export, or just right-click-save each image) and drop them into
  an `/images` folder, then swap them in — happy to help wire this up once you have them.
- **Contact form**: currently points to a placeholder Formspree endpoint. Sign up free at
  formspree.io, create a form, and replace `REPLACE_WITH_YOUR_FORMSPREE_ENDPOINT` in
  `contact.html` with your real endpoint — otherwise the form won't send anywhere yet.
- **Email address**: the old site's email was obscured by Weebly's spam protection and wasn't
  captured — add it to `contact.html` and the footer once you have it handy.
- **Support staff photos/names**: Esther and Siew Poh are named on the About page per the old
  site; add photos if you'd like.
