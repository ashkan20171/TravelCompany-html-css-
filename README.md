# Ashkan Travel — Bilingual Travel Experience

A responsive multi-page travel website built with HTML, CSS, vanilla JavaScript, Bootstrap, and legacy jQuery components.

## Features
- English by default; Persian language switch with RTL/LTR layout and persistent preference
- Seven interconnected travel pages
- Accessible floating travel assistant with locally implemented FAQ responses (no external AI model)
- Responsive visual refinements, semantic controls, SEO description tags
- Preserves original imagery and layout assets

## Run
Open `index.html` in a browser, or serve the folder using `python -m http.server 8000` and visit `http://localhost:8000`.

## Notes and limitations
The English copy for some long Persian template paragraphs is summarized rather than translated literally. The assistant is rule-based and does not call a live LLM. Forms, reservations and payments require a real backend before production use. Replace placeholder business details and verify licensing of inherited assets before deployment.

## Next steps
Connect a secure backend for real booking, newsletter signup and an authenticated AI assistant. Add automated accessibility and browser tests.


## Stage 2 — Destination Explorer

Open `explore.html` for the new searchable, sortable and filterable destination catalog. It includes persistent favorites, EN/FA labels, a demonstration USD/Toman display and a client-side email enquiry composer. **No backend booking, live inventory, payment or AI API is connected.** The Toman conversion uses an explicitly illustrative rate, not market FX. Run with `python -m http.server 8000` and visit `http://localhost:8000/explore.html`.


## Stage 3 — Trip Planner

Open `planner.html` to create a sample itinerary with date, travelers, and travel style. The result can be printed or saved locally in the browser. This is **not** a real booking engine: itinerary suggestions, prices and toman conversions are illustrative. No payment, availability check, or AI API is provided.

### Privacy & security

The trip planner uses `localStorage` only for user-selected preferences; no personal details or payment data are collected. The chatbot is a local rules-based assistant. Do not place API keys in frontend JavaScript. A production AI chatbot needs a backend proxy with authentication, rate limiting, and abuse protections.


## Stage 4: Cinematic visual refresh
- New 3D-inspired floating globe and animated hero, with reduced-motion support.
- Locally hosted cinematic travel background, generated for this project.
- Responsive destination search entry point and bilingual hero copy.
- Dimensional hover treatments, contrast improvements, and mobile layout.
- The visual is a 3D-style rendered image, not an interactive WebGL scene.
- Search opens the destination explorer; server-backed availability and bookings are not implemented.


## Stage 5 — site-wide cinematic backgrounds
Every HTML page now loads `css/global-cinematic.css`, sharing the bundled coastal travel backdrop. The background is viewport-fixed, full-bleed, and covered by translucent contrast-preserving section surfaces. Mobile and reduced-transparency/print fallbacks are included.

## Stage 6 — Brand identity
- Original scalable SVG logo (sun, mountains, plane and ocean) in the shared header of every page.
- Responsive sizing, hover affordance, RTL/LTR-aware spacing, accessible alt text and reduced-motion support.
- Logo asset: `pics/ashkan-travel-logo.svg`; CSS: `css/stage6-brand.css`.

## Stage 7: Glass navigation
Sticky glass header, keyboard-friendly local page search, destination shortcuts, and scroll-to-top. Search is local navigation only, not a booking engine.

## Stage 8: Header hotfix
Fixed malformed list nesting and conflicting flex layouts across all HTML pages. Desktop navigation is horizontal, mobile navigation collapses, and language/RTL behavior is preserved.


## Stage 9 header hotfix

Replaced redundant header quick links with a compact search action, enforced brand-left/navigation-right for English and brand-right for Persian, and improved responsive collapse. Check all pages in a browser after clearing cache. This is a frontend-only project.


## Stage 10 — clean cinematic backgrounds
- Replaced the screenshot-like background (which included fake UI) with a locally bundled, text-free illustrated coastal SVG.
- Applied the clean background to every page and the home hero.
- Added matching navigation on Explorer and Planner with English/Persian labels.
- Preserved the existing features; booking and AI remain demonstrations.

## Stage 11 — Destination discovery polish
- Responsive destination cards with region badges, favorites, sample price disclosure, accessible focus styles and hover motion.
- Improved filter form, enquiry layout and RTL support.
- Fixed conflicting language preferences on the Explorer/Planner navigation; language now uses `ashkan-travel-language` shared with the rest of the site.
- The app remains a static frontend. Prices and currency conversion are illustrative; the enquiry uses the local mail application; the chat is rule-based, not a live AI integration.

## Stage 12 — Tour details

- `tour-details.html?tour=paris|india|netherlands` has bilingual tour descriptions, highlights and suggested daily itineraries.
- Destination Explorer links to detail pages and enquiry links preselect the selected tour.
- Favorites are shared with the Explorer using localStorage.
- English is default; Persian is RTL and stored across pages.
- Tour content, prices, currency conversion and itineraries are demonstration data. No live reservations or payments.


## Stage 13 — travel enquiry wizard
- New `booking.html` with a three-step responsive English/Persian enquiry workflow, live illustrative cost estimate, traveler/date validation and review screen.
- Tour details enquiry buttons now open the wizard and preselect the tour.
- The final action prepares a mailto draft; it does **not** create a booking, send an email automatically, collect payment, or check live availability.
- All prices are illustrative USD amounts and child estimate uses a sample 65% multiplier.


## Stage 14 — My Trips
- `my-trips.html` lists optional saved enquiry drafts, with per-draft and clear-all deletion.
- Booking review step now offers an explicit Save Draft action.
- Only destination, departure date, traveler counts and illustrative cost are stored in this browser; personal contact details are not stored.
- No login, payment, server persistence or confirmed reservation is implied.


## Stage 15 — Travel Preferences
- Added `profile.html`, a bilingual, responsive, local-only travel preference screen.
- Saves style, approximate USD budget and preferred duration in localStorage; includes validation and reset.
- Accessible Preferences shortcut on existing pages.
- No account, real personalization of tour availability, or backend is implied.

## Stage 16 — Personalized Recommendations (local demo)
- New bilingual `recommendations.html` uses saved local preferences to rank the three sample tours.
- Filters for style, USD budget, and duration; if no exact match, alternatives are clearly labeled.
- Direct links to tour details and shortcuts from Preferences, Explorer, and My Trips.
- No external AI API or backend; matching is a transparent rules-based demo.
