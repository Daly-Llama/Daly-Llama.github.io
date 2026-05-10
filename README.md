# Portfolio Setup Guide

Welcome! This guide walks you through getting your portfolio live on GitHub Pages.
No prior web experience needed — follow each step in order.

---

## Your File Structure

When set up correctly, your GitHub repo should look like this:

```
your-repo/
├── _config.yml              ← Site settings (your name, email, links)
├── _layouts/
│   └── default.html         ← Navigation + footer template (rarely edited)
├── assets/
│   └── css/
│       └── style.css        ← ALL colors, fonts, and styling — edit here
├── index.md                 ← Home page
├── about.md                 ← About page
├── projects.md              ← Projects page
└── contact.md               ← Contact page
```

---

## Step 1 — Create Your GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** button (top right) → **New repository**
3. Name it exactly: `yourusername.github.io` (use YOUR actual GitHub username)
4. Set it to **Public**
5. Click **Create repository**

---

## Step 2 — Upload Your Files

**Option A — Upload via GitHub website (easiest for beginners):**

1. Open your new repository on GitHub
2. Click **Add file** → **Upload files**
3. Drag all your portfolio files in. Make sure to preserve the folder structure:
   - `_layouts/default.html` must be inside a `_layouts` folder
   - `assets/css/style.css` must be inside `assets/css/`
4. Click **Commit changes**

**Option B — Use PyCharm with Git (recommended for ongoing editing):**

1. In PyCharm: **Git** → **Clone** → paste your repo URL
2. Copy your portfolio files into the cloned folder
3. **Git** → **Commit** → **Push**

---

## Step 3 — Enable GitHub Pages

1. In your repository, click **Settings** (top menu)
2. In the left sidebar, click **Pages**
3. Under "Source", select **Deploy from a branch**
4. Set Branch to `main` and folder to `/ (root)`
5. Click **Save**

Your site will be live at `https://yourusername.github.io` within 1–2 minutes.

---

## Step 4 — Personalize Your Content

Open each file and look for `<!-- EDIT:` comments — they mark exactly what to change.

### Quick checklist:
- [ ] `_config.yml` — update your name, email, LinkedIn, and GitHub URL
- [ ] `index.md` — update your tagline and card descriptions
- [ ] `about.md` — replace the bio paragraphs with your own words
- [ ] `about.md` — add your profile photo (see below)
- [ ] `projects.md` — fill in your actual projects
- [ ] `contact.md` — update your email and profile links

### Adding your profile photo:
1. Name your photo `profile.jpg`
2. Create an `assets/` folder in your repo (if it doesn't exist)
3. Upload `profile.jpg` into the `assets/` folder
4. The about page will pick it up automatically

---

## How to Change the Visual Style

Everything visual is controlled by CSS variables at the top of `assets/css/style.css`.
Open that file and look for **Section 1** (lines ~30–80).

### To change colors:
```css
--accent:      #0EA5A0;   /* Change this to any color for the teal accents */
--accent-warm: #D97706;   /* Change this for the amber/gold highlights */
--bg-hero:     #1E2A3A;   /* Change this for the dark banner color */
```

### To change fonts:
1. Visit [fonts.google.com](https://fonts.google.com) and pick a font
2. In `_layouts/default.html`, replace the Google Fonts URL with your new font
3. In `style.css`, update `--font-heading` and/or `--font-body`

---

## How to Add a New Page

1. **Create the file:** Copy any `.md` file (e.g., `contact.md`) and rename it (e.g., `blog.md`)
2. **Update the front matter** at the top: change `title:` to your new page name
3. **Add a nav link:** Open `_layouts/default.html`, find the `<ul class="nav-links">` section,
   and paste a new `<li>` block (the comment in that file shows you exactly how)
4. **Write your content** using standard Markdown

---

## Editing Tips

- **Markdown basics:** Use `#` for headings, `**bold**`, `- list items`
- **HTML in Markdown:** GitHub Pages supports HTML inside `.md` files — the styled sections
  (hero, cards, grids) use HTML for layout while regular text uses Markdown
- **After every change:** Commit and push — GitHub Pages rebuilds in ~30 seconds
- **Preview locally (optional):** Install [Jekyll](https://jekyllrb.com/docs/) and run
  `bundle exec jekyll serve` in your project folder to preview before pushing

---

## Getting Help

- GitHub Pages docs: [docs.github.com/pages](https://docs.github.com/en/pages)
- Jekyll docs: [jekyllrb.com/docs](https://jekyllrb.com/docs/)
- Markdown guide: [markdownguide.org](https://www.markdownguide.org/)
