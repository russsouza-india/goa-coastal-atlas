# Goa Coastal Atlas PWA

An interactive Progressive Web App for exploring Goa's coastline, from North Goa through the Central Goa–Panaji pocket to South Goa.

## Project package
The complete app source is included in **`Goa_Coastal_Atlas_PWA.tar.gz`**. It contains the HTML interface, styling, JavaScript application and coastal-location data, PWA manifest, app icon, service worker, and photo-credit register.

## Features
- 50 coastal-location information panels
- North, Central and South Goa coastal circuits
- Interactive map and Google Maps location links
- Geographical learning notes
- Photo credits and licensing review register
- Installable PWA with service-worker app-shell caching
- Automated GitHub Pages deployment

## Live site
After Pages is enabled and the deployment workflow succeeds:
https://russsouza-india.github.io/goa-coastal-atlas/

## Enable GitHub Pages
The connected GitHub Actions token cannot enable the repository's Pages site automatically. Do this once in GitHub:

1. Open **Settings → Pages**.
2. Under **Build and deployment**, choose **GitHub Actions** as the source.
3. Open the **Actions** tab and run or re-run **Deploy Goa Coastal Atlas to GitHub Pages**.

Subsequent pushes to `main` deploy automatically.

## Run locally
Download `Goa_Coastal_Atlas_PWA.tar.gz`, extract it, enter the extracted folder, and run:

```bash
tar -xzf Goa_Coastal_Atlas_PWA.tar.gz
cd goa_coastal_atlas_pwa
python -m http.server 8000
```

Open http://localhost:8000.

## Map, image and accuracy notes
- The interactive basemap uses OpenStreetMap tiles; attribution is shown in the app.
- Google Maps links open location searches for each coastal place.
- Map markers are approximate educational locators, not surveyed coordinates.
- Photo-source and licence status is recorded in `photo_credits_register.csv`. Candidate sources requiring manual review should not be treated as fully verified attributions.
- This is an educational resource, not an official inventory, navigation/safety tool or conservation-permission guide.
- Map tiles and photographs require an internet connection. The service worker caches the app shell, not full offline maps.

## Main references
- Government of Goa – Beaches: https://www.goa.gov.in/what_to_see/beaches/
- Government of Goa – Morjim: https://www.goa.gov.in/places/morjim/
- Government of Goa – Agonda: https://www.goa.gov.in/places/agonda-beach/
- Government of Goa – Palolem: https://www.goa.gov.in/places/palolem-beach/
