# Goa Coastal Atlas PWA

An interactive Progressive Web App for exploring Goa's coastline, from North Goa through the Central Goa–Panaji pocket to South Goa.

## Included
- 50 coastal-location information panels
- North, Central and South Goa coastal circuits
- Interactive map and Google Maps location links
- Geographical learning notes
- Photo credits and licensing review register
- PWA manifest, icon and service worker
- Automated GitHub Pages deployment

## Live site
After the GitHub Pages workflow succeeds:
https://russsouza-india.github.io/goa-coastal-atlas/

## Deployment
The workflow in `.github/workflows/pages.yml` reassembles the source archive from the small text parts in `.github/source-parts/`, verifies its SHA-256 checksum, extracts the app into the Pages artifact, and deploys it.

In GitHub, open **Settings → Pages** and choose **GitHub Actions** as the build and deployment source if it is not already selected. Then check the **Actions** tab for the deployment workflow.

## Local use
Download `Goa_Coastal_Atlas_PWA.tar.gz` from the project release/source package or concatenate the source parts and decode them:

```bash
cat .github/source-parts/part-*.txt | base64 --decode > Goa_Coastal_Atlas_PWA.tar.gz
mkdir goa-atlas
tar -xzf Goa_Coastal_Atlas_PWA.tar.gz --strip-components=1 -C goa-atlas
cd goa-atlas
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
