# DELIVERY — Landing Page

Single-page site for the short film **DELIVERY** (Montréal, 2026).
Design system derived from the crew-call poster: black-dominant screen-print look, poster orange `#E8963C`, cream `#F2E9D8`, Anton/Oswald/Archivo type.

Live site: https://psaad23.github.io/delivery-film/

## Custom domain (later)

1. Add a file named `CNAME` at the repo root containing the domain (e.g. `deliveryfilm.com`).
2. At the registrar, point a CNAME record `www → psaad23.github.io` (and A records for apex: 185.199.108.153 / .109 / .110 / .111).
3. Settings → Pages → set the custom domain + enforce HTTPS.

## Images

The illustrations were generated with Artlist (Nano Banana 2) in the poster's style and are
hot-linked from Artlist's CDN (URLs valid long-term). To vendor them into the repo later,
download each `<img src>` URL from index.html into an `assets/` folder and update the paths:
ride-near / ride-mid / ride-far (21:9) and door-shut / door-ajar / door-open (4:5).

## Animations

Two scroll-driven sequences (script at the bottom of index.html, rAF-loop based, respects
prefers-reduced-motion): the courier recedes into the city as the hero band scrolls out,
and the Tone door plays a 5-stage sequence: shut → ajar → open (woman) → ajar → shut.

## Reusing the look on subpages

Design tokens live in the `:root` block of index.html. For a subpage: copy index.html,
keep `<nav>`, `<footer>`, the token block, and the `.label` / `.rule` / `h2` patterns;
swap the sections in between.
