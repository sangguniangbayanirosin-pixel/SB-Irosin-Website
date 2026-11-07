# Sangguniang Bayan ng Irosin — Website

## Contents
- `index.html` — responsive official website page (single file: HTML, CSS and JS)
- `assets/` — seals, QR codes, the civic/mountain photo (`irosin-civic.jpg`), Mount Bulusan (`irosin-bulusan.jpg`) and the official collage (`hero-collage-web.jpg`)

## Publish with GitHub Pages
1. Open the GitHub repository.
2. Replace the existing `index.html` and `assets/` folder with the contents of this package.
3. Commit the changes to the `main` branch.
4. Open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/(root)`, then Save.
5. Check the **Actions** tab for a successful Pages deployment.

## What changed in this update
- **Name corrected everywhere to “Hon. Jesus L. Borlagdan”** (leadership row, barangay assignments, committees, search). The old “source-name discrepancy” notice was removed.
- **Hero:** opens on the official collage with the headline in place. The background then changes by itself every 3.6 seconds (collage → municipal building → Mount Bulusan and rice fields) and also changes as the visitor scrolls through the hero. Only the background cross-fades; the headline, buttons and node network keep running. Small dots at the bottom right show progress and let visitors pick a background.
- **Node network** (35–60 drifting nodes, the cursor is one more node) behind the hero text.
- **Header** slides away on scroll down and returns on the first scroll up.
- **Vision / Mission / Quality Policy** cards pin one after another with an 80px offset and shrink as the next one slides over. Their text is centered.
- **Committees & Barangay Assignments** use a light-blue gradient with violet neon-style outlines. Also fixed: filtering the Barangay Assignments tab now really hides non-matching cards.
- **Bento grid** (Legislative Records): hovered tile grows to 1.04, the others dim to 0.42 opacity and shrink to 0.94, with a spring.
- **Folded-paper sidebar** (“Sections” tab): two 160px panels on a 3D hinge (rotateY 62° and −124°) collapse into a thin strip.
- **Leadership** is a full-screen pinned section: vertical scroll moves the row of cards sideways, with a thin progress bar underneath (GSAP ScrollTrigger).

## Notes
- GSAP 3.12.5 and ScrollTrigger load from cdnjs. If they can’t load (offline/blocked), the leadership row becomes a normal swipeable row with the same progress bar. Google Fonts and the Facebook embed also need an internet connection.
- `prefers-reduced-motion: reduce`: the hero stays on the collage (no cycling, no pinning), cards don’t shrink, the network is drawn as a still frame, and the leadership row is not pinned.
