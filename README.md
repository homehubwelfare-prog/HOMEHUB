# HOMEHUB — website prototype

A responsive, front-end website based on the uploaded HOMEHUB pitch PDF: property discovery, people/property trust concepts, locality context, rent/buy filters, distance estimates, Google Maps links, comparison details and a simple listing editor.

## Files and languages

- `index.html` — HTML5 (page structure)
- `style.css` — CSS3 (responsive visual design)
- `properties.js` — JavaScript data file containing 20 illustrative sample listings
- `app.js` — JavaScript (filters, cards, distance estimate, Google Maps links, details modal)
- `admin.html` — HTML5 (listing manager page)
- `admin.js` — JavaScript (browser-only edit form)
- `README.md` — setup and deployment guide

## Run locally

1. Extract the ZIP.
2. Open the `HOMEHUB` folder in VS Code.
3. Install the VS Code **Live Server** extension (Ritwick Dey).
4. Right-click `index.html` → **Open with Live Server**.

Opening `index.html` directly may also work, but Live Server is better for testing.

## Put it online for free (static demo)

### GitHub Pages
1. Create/sign in to GitHub and create a new **public** repository, e.g. `homehub-demo`.
2. Upload all files in this folder (not the ZIP itself): `index.html`, `style.css`, `app.js`, `properties.js`, `admin.html`, `admin.js`, `README.md`.
3. Repository → **Settings** → **Pages**.
4. Under Build and deployment, select **Deploy from a branch**, choose `main` and `/ (root)`, then Save.
5. Wait for the Pages URL to appear. It will look like `https://YOUR-USERNAME.github.io/homehub-demo/`.

This hosts a static prototype. Browser-only admin edits are not shared with other visitors.

## What works in this prototype

- 20 sample listings across different Indian cities/states.
- Rent / buy, city/state/locality, budget, bedroom and sort filters.
- Listing detail modal.
- Browser location permission: calculates approximate straight-line distance from your current device location to sample coordinates.
- Google Maps search link for each listing.
- Listing manager lets you edit title, location, price, mode, bedrooms, bathrooms, area, coordinates, photo URL, notes and verification label in the same browser.
- Responsive design for phone and laptop.

## Important limits before a real launch

- **All properties, prices, coordinates, and locality notes are demo examples, not verified live listings.** The photos are illustrative exterior/interior reference photos from Unsplash and are not guaranteed to show the actual listed property or its exact locality.
- Distances are straight-line estimates, not driving/walking distances. Google Maps opens to let the visitor check routes and travel time.
- The browser geolocation prompt only works on HTTPS or localhost and requires user permission.
- Google Maps links work without an embedded Google Maps API key. An interactive embedded map with pins, Places nearby, route distance/time, and geocoding requires Google Maps Platform API setup and billing; restrict the API key by website/referrer and enable only needed APIs.
- The admin page uses `localStorage`: it is not secure, is not a real admin login, and edits are visible only in that same browser. A production version needs a backend and database (e.g. Firebase/Supabase), authenticated admin access, image storage, validation, backups and server-side rules.
- Verification, emergency SOS, complaint reports, owner/tenant KYC, legal checks, payments and AI matching are not operational in this prototype. These need secure services, consent, safeguards and testing before real users rely on them.
- Do not present sample listings as available homes or collect advance payments against them.

## Suggested production roadmap

1. Validate the visual MVP and filters.
2. Replace sample data with consented, owner-submitted listings and moderation.
3. Add database + secure admin login + image upload.
4. Add Maps API for pins, nearby essentials and route travel time.
5. Build document/owner verification workflow with audit records.
6. Add reporting, privacy policy, terms, consent and emergency feature review.
7. Test mobile performance, accessibility, security and data protection before launch.

The PDF describes a vision and proposed features, not a live property database or operational verification system. This prototype reflects the concept without claiming those services are already active.
