# Migration to genuine al-folio v1.1

This package is an **overlay for the official al-folio v1.1 template**.
It is not a standalone HTML theme.

## Why this is different from the previous portfolio

The official al-folio v1.1 site uses:

- Jekyll
- al-folio plugin architecture
- `_pages/` for navigation pages
- `_projects/` as a Jekyll collection
- `_bibliography/papers.bib` with Jekyll Scholar
- `_data/cv.yml` for the CV page
- `_data/socials.yml` for contact/social icons
- GitHub Actions for build and deployment

## Safest migration for your existing `wuzhenhuang.github.io`

### 1. Keep your current site as a backup

Rename the current repository temporarily, for example:
`wuzhenhuang.github.io-static-backup`

Do not delete it until the new al-folio deployment works.

### 2. Create a fresh site from the official template

Open:
`alshedivat/al-folio`

Choose:
**Use this template → Create a new repository**

Create a temporary repository, for example:
`wuzhen-al-folio`

Use the official **v1.1** starter.

### 3. Apply this overlay

Copy the contents of this ZIP into the root of the fresh al-folio repository.

Replace the template demo files with:

- `_pages/about.md`
- `_pages/research.md`
- `_pages/publications.md`
- `_pages/experience.md`
- `_pages/cv.md`
- `_projects/*`
- `_bibliography/papers.bib`
- `_data/cv.yml`
- `_data/socials.yml`
- `_data/repositories.yml`
- `assets/img/*`

Delete or disable demo navigation pages that you do not want to show, especially:

- blog
- repositories
- books
- teaching
- people
- projects (the custom `research` page replaces it)

The final navbar should be:
**About | Research | Publications | Experience | CV**

### 4. Edit `_config.yml`

Follow `CONFIG_EDIT.md`.
Do not replace the entire v1.1 configuration.

Important:

- `url: https://wuzhenhuang.github.io`
- `baseurl:` must be empty for the final personal-site repository
- `al_folio.distill.allow_remote_loader: false`

### 5. Add your CV PDF

Place your current PDF at:
`assets/pdf/Wuzhen_Huang_CV.pdf`

### 6. Test in the temporary repository

Enable GitHub Actions and let al-folio build/deploy.

For the temporary repository, its `baseurl` must temporarily be:
`/wuzhen-al-folio`

When testing is complete, change it back to empty before moving to the personal-site repository.

### 7. Switch to your final GitHub Pages URL

After the new site builds successfully:

- keep the old static repo as backup
- rename the new al-folio repo to `wuzhenhuang.github.io`
- ensure `_config.yml` has:
  - `url: https://wuzhenhuang.github.io`
  - `baseurl:`

The site will then publish at:
`https://wuzhenhuang.github.io/`

## Updating later

### Add/edit a research project

Edit:
`_projects/*.md`

### Add a publication

Edit:
`_bibliography/papers.bib`

### Edit homepage bio

Edit:
`_pages/about.md`

### Edit experience

Edit:
`_pages/experience.md`

### Edit generated CV

Edit:
`_data/cv.yml`

### Replace project images

Replace files in:
`assets/img/`

No handwritten `index.html` is needed in the genuine al-folio setup.
