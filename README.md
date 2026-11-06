# Chinmay Paranjape — Portfolio

Personal portfolio website of Chinmay Paranjape, Senior Data Scientist.
It's a static site: plain HTML, CSS and JavaScript, so there's no build step and no dependencies.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site (Home, Projects, Experience, Education, Writing, Contact) |
| `Chinmay_Paranjape_Resume.pdf` | Résumé served by the "Download résumé" button |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |

## Publish on GitHub Pages

1. Create a new repository on GitHub. Name it `<your-username>.github.io` to get the address `https://<your-username>.github.io`, or use any name (e.g. `portfolio`) to get `https://<your-username>.github.io/portfolio`.
2. Upload every file in this folder to the repository root: **Add file → Upload files**, drag them in, then **Commit changes**.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose branch `main` and folder `/ (root)`, then **Save**.
4. After a minute or two, your site's address appears at the top of the Pages settings.

### Custom domain (optional)
In **Settings → Pages → Custom domain**, enter your domain (e.g. `chinmayparanjape.com`), then add the DNS records GitHub shows at your domain registrar. Tick **Enforce HTTPS** once it's available.

## Run locally
Open `index.html` in a browser, or serve the folder:
```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Updating content
All content lives in the **CONTENT** block at the top of the `<script>` in `index.html`:

- `PROFILE`: name, title, email, LinkedIn, Medium, GitHub (an empty `github` hides the link), optional photo, résumé file name
- `IMPACT`: headline numbers on the homepage
- `EXPERTISE`, `SKILLS`
- `EXPERIENCE`: one object per role
- `EDUCATION`, `ACHIEVEMENTS`, `CERTIFICATIONS`
- `PROJECTS`: professional case studies. Each gets its own page at `#project-<id>`; `featured: true` shows it on the homepage. Optional fields (`dataset`, `challenges`, `learnings`, `workflow`) are hidden when empty.
- `PERSONAL_PROJECTS`: independent projects (`title`, `intro`, `tools`, `github`, `demo`)
- `ARTICLES`: Medium articles (`title`, `url`, `date` as `YYYY-MM-DD`, `excerpt`, `category`, `readingTime`, `image`)

### Replace the résumé
Overwrite `Chinmay_Paranjape_Resume.pdf` with a file of the same name and commit it.

### Add a photo later (optional)
Upload an image (e.g. `portrait.jpg`, portrait-shaped) and set `photo: "portrait.jpg"` in `PROFILE`. Leave `photo: ""` for no photo.

## Note
The downloadable résumé currently includes a phone number. Replace the PDF if you don't want that public.
