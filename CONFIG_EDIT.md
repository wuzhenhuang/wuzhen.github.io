# Required edits to the OFFICIAL al-folio v1.1 `_config.yml`

Do **not** replace the whole official `_config.yml` with a shortened file.
Keep the v1.1 starter configuration and change only these values.

```yaml
title: blank
first_name: Wuzhen
middle_name:
last_name: Huang

contact_note: >
  For research and R&D opportunities, please contact me by email.

description: >
  Research portfolio of Wuzhen Huang: X-ray imaging, computational CT,
  advanced manufacturing, process monitoring, sensing and signal processing,
  materials characterization, NDT, metrology, and quantitative engineering.

footer_text: >
  Powered by <a href="https://jekyllrb.com/" target="_blank">Jekyll</a>
  with the <a href="https://github.com/alshedivat/al-folio" target="_blank">al-folio</a> theme.

keywords: x-ray imaging, xct, computed tomography, computational imaging, advanced manufacturing, process monitoring, signal processing, materials characterization, metrology
lang: en
icon: 🔬

url: https://wuzhenhuang.github.io
baseurl:

navbar_fixed: true
footer_fixed: false
search_enabled: true
socials_in_search: true
posts_in_search: false
bib_search: true
max_width: 930px

al_folio:
  api_version: 1
  style_engine: tailwind
  tailwind:
    version: 4.1.18
    preflight: false
    css_entry: assets/tailwind/app.css
  distill:
    engine: distillpub-template
    source: al-org-dev/distill-template#al-folio
    allow_remote_loader: false
  features:
    cv:
      enabled: true
    distill:
      enabled: true
  compat:
    bootstrap:
      enabled: false
      support_window: v1.0-v1.2
      deprecates_in: v1.3
      removed_in: v2.0
  upgrade:
    channel: stable
    auto_apply_safe_fixes: false
```

In the existing `scholar:` block, change only:

```yaml
scholar:
  last_name: [Huang]
  first_name: [Wuzhen, W.]
```

Keep these official features enabled:

```yaml
enable_darkmode: true
enable_project_categories: true
enable_math: true
enable_medium_zoom: true
lazy_loading_images: true
```

Recommended for this portfolio:

```yaml
enable_navbar_social: false
serve_og_meta: true
serve_schema_org: true
```

The v1.1 security setting `al_folio.distill.allow_remote_loader` should remain `false`.
