# Cape Island Taxi — SAMPLE booking site (demo)

Front-end-only mock of a local taxi booking site for Falmouth / East Falmouth, MA. **Not a live service** — no real bookings, payments, texts or calls.

## Features (all mock, saved in browser localStorage)
- Fare estimate: $3.00 flag + $3.75/mile (Town-approved tariff). Labeled "Estimate — final fare is by the meter." No night/surge/wait fees, no flat rates.
- Preset local stops (Walmart, Falmouth Hospital, Bus Depot, Woods Hole Ferry…) with approximate miles
- Book now, future reservation (date/time), cash/card, SMS opt-in, text-or-call confirmation (fake toast)
- Trip status mock: assigned → ~5 min (map unlock) → driver here
- Preferences page

## Run locally
Open `index.html` in a browser, or `python3 -m http.server` and visit http://localhost:8000.

## GitHub Pages
Served from `main` branch, root folder. Custom domain to be wired later.

## Not wired yet
Supabase (accounts/bookings), Square prepay, SMS/calls, GPS map, real business phone (placeholder (508) 555-0199).

## Square card payments (setup)
1. `cp config.example.js config.js` (config.js is gitignored).
2. Paste your Square **Application ID** and **Location ID** (Square Developer Dashboard) and set `SQUARE_ENV`.
3. With values set, the Card option loads the Square Web Payments SDK and tokenizes the card. Without them, a demo "Simulate card paid" button is shown.
4. A real charge still needs a server (e.g. Supabase Edge Function calling Square Payments/Checkout API) to exchange the token — being wired next. Note: because GitHub Pages deploys only committed files, go-live needs the IDs committed (App ID + Location ID are public-safe; the Access Token must never be in this repo).

Rider discount flags (Senior/Disability/Veteran/Wheelchair) are dispatch tags only and never change the estimate. Loyalty points are a localStorage demo; redeem is not applied to fares.

## Theme
Morning theme with faded Woods Hole lighthouse (assets/woods-hole-light.jpg, generated illustration). No demo banner or rates on the booking sheet (meter fare; tariff in Info). Weekly work rides: 3/5/10 pack, 10% off only when prepaid (company sample offer). Ferry drop-off & pickup for Martha’s Vineyard.
