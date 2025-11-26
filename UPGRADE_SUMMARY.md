---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.3.4-beta
- **To:** 0.5.0-beta
- **Date:** 2025-11-26
- **Automated changes:** 86
- **Manual steps:** 18

## Automated Changes Applied

### Configuration (2 files)

- [x] Added story_interface configuration section to _config.yml
- [x] Updated _config.yml: version 0.5.0-beta (2025-11-26)

### Layouts (16 files)

- [x] Updated story layout (multilingual, widgets)
- [x] Updated object layout (multilingual)
- [x] Updated objects index layout (multilingual)
- [x] Updated default layout (multilingual)
- [x] Updated glossary layout (multilingual)
- [x] Updated glossary index layout (multilingual)
- [x] Updated page layout
- [x] Updated index layout (multilingual)
- [x] Updated index layout (site description link styling)
- [x] Updated object layout (coordinate picker buttons)
- [x] Updated story layout (mobile responsive features restored)
- [x] Updated telar styles (mobile responsive features, gallery layout)
- [x] Updated _layouts/index.html: Updated index layout (site description link styling)
- [x] Updated _layouts/story.html: Embed mode support, share button
- [x] Updated _layouts/index.html: Share button in navbar
- [x] Updated _layouts/default.html: Share panel modal

### Includes (9 files)

- [x] Updated story-step include (multilingual)
- [x] Updated panels include (widgets support)
- [x] Updated viewer include
- [x] Updated header include (multilingual)
- [x] Updated footer include (multilingual, theme attribution)
- [x] Updated _includes/share-button.html: Share button component
- [x] Updated _includes/share-panel.html: Share/embed modal
- [x] Updated _includes/header.html: Navbar share button
- [x] Updated _includes/panels.html: Mobile image width fix

### Styles (3 files)

- [x] Updated telar styles (widgets, mobile responsive, site description links)
- [x] Updated assets/css/telar.scss: Updated CSS (mobile navbar, font sizes, title wrapping)
- [x] Updated assets/css/telar.scss: Embed mode, share UI, carousel, mobile fixes

### Scripts (12 files)

- [x] Updated story JavaScript
- [x] Updated telar JavaScript (glossary auto-linking)
- [x] Added widgets JavaScript (carousel, tabs, accordion)
- [x] Updated objects.json endpoint
- [x] Updated story JavaScript (mobile navigation, preloading, transitions)
- [x] Removed unused file: assets/js/scrollama.min.js
- [x] Removed unused file: assets/js/openseadragon.min.js
- [x] Updated scripts/csv_to_json.py: CSV-driven processing, flattened paths
- [x] Updated scripts/generate_iiif.py: Extended format support, case-insensitive
- [x] Updated assets/js/embed.js: Embed mode detection and banner
- [x] Updated assets/js/share-panel.js: Share/embed functionality
- [x] Updated assets/js/story.js: Embed navigation, panel fixes

### Documentation (10 files)

- [x] Updated README
- [x] Updated README (supporter acknowledgments)
- [x] Updated README.md: Updated README (version 0.4.2-beta)
- [x] Removed deprecated directory: docs/google_sheets_integration
- [x] Updated README.md: v0.5.0 documentation
- [x] Updated components/README.md: Updated directory structure
- [x] Updated components/images/README.md: Flattened structure documentation
- [x] Updated components/pdfs/README.md: Future v0.6.0 placeholder
- [x] Updated components/audio/README.md: Future v0.7.0 placeholder
- [x] Updated components/3d-models/README.md: Future v0.8.0 placeholder

### Other (34 files)

- [x] Created _data/languages directory
- [x] Added English language file (_data/languages/en.yml)
- [x] Added Spanish language file (_data/languages/es.yml)
- [x] Updated IIIF URL warning (multilingual)
- [x] Added accordion widget template
- [x] Added carousel widget template
- [x] Added tabs widget template
- [x] Updated CSV processor (IIIF metadata extraction)
- [x] Updated collection generator (widgets, glossary)
- [x] Updated IIIF tile generator
- [x] Updated Python requirements
- [x] Updated Austin theme (creator attribution)
- [x] Updated Neogranadina theme (creator attribution)
- [x] Updated Paisajes theme (creator attribution)
- [x] Updated Santa Barbara theme (creator attribution)
- [x] Added upgrade notice to index.md
- [x] Added 'Development & Testing' section with testing-features
- [x] Updated English language file with coordinate picker strings
- [x] Updated Spanish language file with coordinate picker strings
- [x] Updated CHANGELOG
- [x] Updated .github/workflows/build.yml: Updated build workflow (smart IIIF detection with caching)
- [x] Discovered 0 CSV-referenced images
- [x] Found 0 image references in .md files
- [x] Removed empty directory: components/images/objects
- [x] Removed empty directory: components/images/additional
- [x] Migrated 79 images to flat structure
- [x] No image path updates needed
- [x] Updated objects.csv: Renamed 'iiif_manifest' column to 'source_url'
- [x] Created directory: components/pdfs
- [x] Created directory: components/audio
- [x] Created directory: components/3d-models
- [x] Updated _data/languages/en.yml: Share/embed strings, updated error messages
- [x] Updated _data/languages/es.yml: Spanish translations
- [x] Updated CHANGELOG.md: v0.5.0 changelog

## Manual Steps Required

Please complete these after merging:

1. Review multilingual configuration in _config.yml (telar_language: "en" or "es") ([guide](https://ampl.clair.ucsb.edu/telar-docs/multilingual-setup))
2. Optionally add widgets to your stories (carousel, tabs, accordion) ([guide](https://ampl.clair.ucsb.edu/telar-docs/widgets))
3. Optionally create glossary terms and add [[term]] links to your content ([guide](https://ampl.clair.ucsb.edu/telar-docs/glossary))
4. Test IIIF metadata auto-population by leaving object fields blank in CSV ([guide](https://ampl.clair.ucsb.edu/telar-docs/iiif-metadata))
5. Add theme creator attribution to your theme YAML file (optional) ([guide](https://ampl.clair.ucsb.edu/telar-docs/themes#creator-attribution))
6. Run "bundle exec jekyll build" to test your upgraded site
7. Update your upgrade workflow file (one-time fix to prevent config comment deletion): (1) Go to https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/upgrade.yml (2) Select all (Ctrl/Cmd+A) and copy (3) In your repository, navigate to .github/workflows/upgrade.yml (4) Click the pencil icon to edit (5) Select all existing content and delete it (6) Paste the new content (7) Scroll to bottom and click "Commit changes". This fixes a bug that was stripping documentation comments from your _config.yml file during upgrades. ([guide](https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/upgrade.yml))
8. Run "bundle exec jekyll build" to test your upgraded site
9. Test mobile responsive features on small screens (optional)
10. Try the new coordinate picker buttons in object pages (optional)
11. CRITICAL: The updated build.yml workflow must be merged/committed for IIIF caching to work. If using automated upgrade workflow: Review and MERGE the upgrade pull request - the new build workflow will not take effect until merged. If upgrading locally: COMMIT and PUSH .github/workflows/build.yml - the new workflow is not active until pushed to GitHub. Until the new workflow is active, the IIIF caching protection is not in effect.
12. Test the smart IIIF detection: Make a content-only change (edit a story markdown file), push to GitHub, and verify the build workflow completes faster by skipping IIIF regeneration (optional)
13. ⚠️ **CRITICAL: Update Your GitHub Actions Workflows** ⚠️

**Without this step, images will NOT display on your published site.**

The upgrade changed where images are stored, but your GitHub Actions workflows still point to the old location. You must update two files: `build.yml` and `upgrade.yml`.

---

**Option 1: Using the GitHub Website**

1. Go to the Telar repository workflows: https://github.com/UCSB-AMPLab/telar/tree/main/.github/workflows
2. Click on `build.yml`, then click the "Raw" button, and copy all the text
3. In **your** repository on GitHub, go to `.github/workflows/build.yml`
4. Click the pencil icon (✏️) to edit, delete everything, and paste the new content
5. Click "Commit changes" at the bottom
6. Repeat steps 2-5 for `upgrade.yml`

---

**Option 2: Using the Command Line** (if you've been syncing your repository to your machine and are comfortable with git)

Run these commands in your repository:

```bash
# Download the updated workflows
curl -o .github/workflows/build.yml https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/build.yml
curl -o .github/workflows/upgrade.yml https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/upgrade.yml

# Commit the changes
git add .github/workflows/
git commit -m "Update workflows for v0.5.0 image structure"
git push
```

**That's it!** Your next build will use the correct image locations. ([guide](https://github.com/UCSB-AMPLab/telar/tree/main/.github/workflows))
14. Regenerate IIIF tiles to ensure images work with new structure: python3 scripts/generate_iiif.py
15. Test your site build: bundle exec jekyll build
16. Test embed mode: Add ?embed=true to any story URL to see the embed mode UI with navigation banner
17. Explore new share/embed UI: Click the share button (icon with arrow) on stories or homepage to access share links and embed code
18. Optional: Install pillow-heif for HEIC/HEIF support (iPhone photos). Run: pip install pillow-heif. The framework gracefully degrades if not installed, converting HEIC to standard formats.

## Resources

- [Full Documentation](https://ampl.clair.ucsb.edu/telar-docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
