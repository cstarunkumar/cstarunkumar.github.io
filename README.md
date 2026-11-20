# C S Tarun Kumar

Personal academic website and portfolio hosted at [cstarunkumar.github.io](https://cstarunkumar.github.io).

Built with [Jekyll](https://jekyllrb.com/) and GitHub Pages, themed with a customized Everforest palette, retro-modern typography, and LaTeX KaTeX support.

---

## Sections & Highlights

- **About**: Profile, education in Computer Science & Engineering at [Vellore Institute of Technology, Vellore](https://vit.ac.in/), interests, and contact details.
- **Notes**: Course notes, study summaries, and independent learning resources (e.g. Computer Science, Mathematics, Electrical Engineering, Computational Chemistry) with integrated **PDF** and **LaTeX (.tex)** download options.
- **Projects**: Showcase of academic, engineering, and open-source software projects.
- **Publications & Bookshelf**: Academic bibliography and personal reading lists.
- **Theme & Design**: Custom Everforest palette with dual light/dark modes, retro typography, and responsive mobile navigation.

---

## Local Development

To run and preview the site locally:

```bash
# 1. Clone repository
git clone https://github.com/cstarunkumar/cstarunkumar.github.io.git
cd cstarunkumar.github.io

# 2. Install dependencies
bundle install

# 3. Start local development server
bundle exec jekyll serve --livereload
```

Open `http://localhost:4000/` in your browser.

---

## Adding New Notes

To publish a note, add a Markdown file to `_notes/`:

```yaml
---
layout: note
title: Note Title
description: Brief summary of topic
category: college # or 'self-study'
course: COURSE_CODE
date: YYYY-MM-DD
tags: [tag1, tag2]
pdf: /assets/pdf/my_note.pdf   # optional
tex: /assets/tex/my_note.tex   # optional
---
```

When pushed to GitHub, GitHub Actions compiles the note into an HTML page with automatic PDF and TeX download buttons.

---

## Deployment

The site is continuously built and published via GitHub Actions (`.github/workflows/deploy.yml`) on every push to the `main` branch.

## License

Content &copy; C S Tarun Kumar. Code licensed under the [MIT License](LICENSE).
