# Shubhajit Das academic website

This is an AcademicPages-style GitHub Pages website using the Minimal Mistakes Jekyll theme.

## Deploy to GitHub Pages

```bash
git clone git@github.com:dosshubha/dosshubha.github.io.git
cd dosshubha.github.io
```

Back up the current site:

```bash
git checkout -b backup-current-site
git push origin backup-current-site
git checkout main
```

Copy the files from this folder into the repository root, then:

```bash
git add .
git commit -m "Build academic website"
git push origin main
```

GitHub Pages should build the site automatically at https://dosshubha.github.io/.

## Edit pages

- Home: `index.md`
- Research: `_pages/research.md`
- Publications: `_pages/publications.md`
- Teaching: `_pages/teaching.md`
- CV: `_pages/cv.md`
- Contact: `_pages/contact.md`
- Profile photo: `assets/images/shubhajit_das.jpg`
- CV PDF: `files/Shubhajit_Das_CV.pdf`
