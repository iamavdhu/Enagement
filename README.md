# Omkar & Rutuja — Engagement Invitation

A single-page engagement invitation website with a live countdown, photo gallery, and scroll animations — built for Omkar & Rutuja's engagement ceremony on **13 September 2026** in Karad, Maharashtra.

## 🔗 Live Preview

Once deployed (see below), your site will be available at:
`https://<your-github-username>.github.io/<repo-name>/`

## 📁 Project Structure

```
omkar-rutuja-engagement/
├── index.html          # The entire site (HTML + CSS + JS in one file)
├── images/              # Photos used in the hero, story, and gallery sections
│   ├── couple-01.jpg
│   ├── couple-02.jpg
│   ├── couple-03.jpg
│   ├── couple-04.jpg
│   ├── couple-05.jpg
│   └── couple-06.jpg
└── README.md
```

## ✏️ How To Edit

Everything lives in `index.html` — no build step, no dependencies to install.

| What to change | Where to look |
|---|---|
| Couple names, date, city | `<section class="hero">` near the top of the `<body>` |
| Countdown target date/time | Near the bottom, in `<script>`: `const target = new Date('2026-09-13T18:00:00');` |
| "Our Story" text | `<section class="story">` |
| Ceremony date / time / venue | `<section class="ceremony">`, inside the three `.card` blocks |
| Gallery photos | Replace files in `images/`, keeping the same filenames — or update the `src`/`data-full` paths in `<section class="gallery">` |
| Closing gift note | `<section class="gift">` |

To swap a photo, just replace the file in `images/` with a new one **using the same filename**, or edit the `src="images/..."` paths directly in `index.html`.

## 🚀 Deploy With GitHub Pages (free hosting)

1. Create a new repository on GitHub and upload this whole folder (or push it with git — see below).
2. In your repo, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`.
4. Choose the `main` branch and `/ (root)` folder, then **Save**.
5. Wait a minute, then visit `https://<your-username>.github.io/<repo-name>/` — your invitation is live.

### Using git from the command line

```bash
cd omkar-rutuja-engagement
git init
git add .
git commit -m "Initial commit: engagement invitation site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then follow steps 2–5 above to enable Pages.

## 🛠 Notes

- The site uses Google Fonts (Cormorant Garamond, Jost) loaded via CDN — an internet connection is required for fonts to display correctly.
- The RSVP form was replaced with a "Your Presence Is Our Present" note — there's no backend, so no data is collected anywhere on the page.
- Fully responsive — tested down to mobile widths (~375px).
- Respects `prefers-reduced-motion` for visitors who've turned off animations at the OS level.
