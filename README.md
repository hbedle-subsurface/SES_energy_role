# OU SES — "What's Your Energy Role?" Quiz

A mobile-first, standalone quiz for recruiting undergraduate students into the [Sustainable Energy Systems Certificate Program](https://ou.edu/mcee/ses) at the University of Oklahoma.

**Live demo** → deploy to GitHub Pages (instructions below)

---

## What it does

A 5-question personality-style quiz that shows undergraduates — especially non-STEM students in journalism, business, pre-law, social sciences, fine arts, and education — how their major and interests connect to the energy future. Each result includes:

- A named career role with description
- A "Why SES fits your path" explanation tailored to their discipline
- A scholarship callout ($1,000 undergraduate awards, no GPA minimum)
- Direct links to `ou.edu/mcee/ses` and `SES@ou.edu`

---

## Files

```
ses-quiz/
├── index.html    ← the entire quiz (self-contained, no build step)
└── README.md     ← this file
```

Everything — HTML, CSS, and JS — lives in `index.html`. No build process, no dependencies to install, no server required. Google Fonts and Tabler Icons load from CDN.

---

## Deploy to GitHub Pages (5 minutes)

### Option A — New repository

1. Go to [github.com/new](https://github.com/new)
2. Create a repository (e.g. `ses-energy-quiz`). Public or Private both work.
3. Upload `index.html` and `README.md` via the GitHub web interface (drag and drop).
4. Go to **Settings → Pages**
5. Under **Source**, select **Deploy from a branch** → branch: `main` → folder: `/ (root)`
6. Click **Save**. Your quiz will be live at:
   ```
   https://<your-username>.github.io/ses-energy-quiz/
   ```

### Option B — Command line

```bash
git init
git add index.html README.md
git commit -m "Add SES energy role quiz"
git branch -M main
git remote add origin https://github.com/<your-username>/ses-energy-quiz.git
git push -u origin main
```

Then enable Pages in repo Settings as above.

### Custom domain (optional)

To serve from e.g. `quiz.ou.edu`:

1. Add a `CNAME` file in the repo root containing your domain:
   ```
   quiz.ou.edu
   ```
2. Configure your DNS CNAME record to point to `<your-username>.github.io`
3. Enable HTTPS in Pages settings once DNS propagates (~10 min)

---

## Linking from a QR code / poster

Once deployed, generate a QR code pointing to your GitHub Pages URL at any free QR generator (e.g. [qr-code-generator.com](https://www.qr-code-generator.com)). The quiz is fully mobile-optimized — students can complete it on their phone in under 90 seconds.

---

## Updating content

All quiz content is in the `<script>` block at the bottom of `index.html`.

| Variable | What it controls |
|---|---|
| `QUESTIONS` | The 5 quiz questions and answer options |
| `RESULTS` | The 5 result cards (title, description, SES pitch, disciplines) |
| Scholarship details | Search for `schol-card` in the HTML to update award amounts / availability |

### Changing the scholarship amount

Search for `$1,000` and update both instances (the intro banner and the result card).

### Adding / removing a question

Add or remove an object from the `QUESTIONS` array. The progress bar auto-calculates based on `QUESTIONS.length`.

---

## Design notes

- **Typefaces**: DM Serif Display (headings) + DM Sans (body) — loaded from Google Fonts
- **Icons**: Tabler Icons outline set — loaded from jsDelivr CDN
- **Colors**: OU Crimson `#8B1A1A`, Forest Green `#1D3A2A`, Gold `#C8922A`, Cream `#FAF7F2`
- **Background**: CSS radial gradient mesh — no images required
- **Mobile-first**: designed for 375px viewport, scales up gracefully to desktop
- **Accessibility**: semantic HTML, `aria-pressed` on option buttons, visible focus states, `role="main"`, screen-reader label on start button

---

## Contact

**Heather Bedle, Director** — Sustainable Energy Systems Certificate Program  
[SES@ou.edu](mailto:SES@ou.edu) · [ou.edu/mcee/ses](https://ou.edu/mcee/ses)
