# Goa Coastal Atlas PWA

An interactive student-facing Progressive Web App for exploring 50 named coastal locations along Goa's shoreline, from North Goa through the Central Goa–Panaji pocket to South Goa.

## What is included
The complete application source and data are preserved in `Goa_Coastal_Atlas_PWA.tar.gz`. The GitHub Pages workflow extracts this archive during deployment, so the published site contains the actual app files rather than only the archive.

- Interactive coastline map with coastal location markers
- 50 beach and coastal-location information panels
- North, Central and South Goa circuits
- Google Maps location links
- Geographical learning notes and fieldwork prompts
- Photo attribution and licensing register
- PWA manifest, app icon and service worker for installation and app-shell caching

## Live site
After the first successful GitHub Pages deployment:
https://russsouza-india.github.io/goa-coastal-atlas/

## Deployment
The workflow at `.github/workflows/pages.yml` deploys automatically on each push to `main`.

In the repository, open **Settings → Pages** and set the build and deployment source to **GitHub Actions** if it is not already selected. Then open **Actions** and check the “Deploy Goa Coastal Atlas to GitHub Pages” run.

## Local use
Extract `Goa_Coastal_Atlas_PWA.tar.gz`, enter the extracted folder, and run:

```bash
python -m http.server 8000
```

Open http://localhost:8000.

## Map, image and accuracy notes
- The interactive base map uses OpenStreetMap tiles (attribution appears in the app).
- Each location includes a Google Maps search link.
- Marker coordinates are approximate educational locators, not surveyed coordinates. Validate them against local sources before formal institutional use.
- Photo-source and licence review status is recorded in `photo_credits_register.csv`. Candidate links that still require manual verification should not be treated as fully verified attributions.
- The app is a learning resource, not an official beach inventory, navigation/safety tool, or conservation-permission guide.
- Map tiles and photographs require internet access; the service worker caches the app shell, not full offline maps.

## Main sources
- Government of Goa – Beaches: https://www.goa.gov.in/what_to_see/beaches/
- Government of Goa – Morjim: https://www.goa.gov.in/places/morjim/
- Government of Goa – Agonda: https://www.goa.gov.in/places/agonda-beach/
- Government of Goa – Palolem: https://www.goa.gov.in/places/palolem-beach/
- Goa Forest Department / Goa University, 2023 mangrove and intertidal mudflat report: https://forest.goa.gov.in/sites/default/files/2024-04/Conservtion%20and%20management%20of%20mangroves_0.pdf
