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
