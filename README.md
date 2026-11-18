# DRMZ On Pockets storefront

A responsive, buildless storefront using the supplied DRMZ logo and the Toykoo homepage as a visual reference. The page recreates the reference's white showroom, outlined vehicle names, black navigation, scale cards, product grids, dark feature section and red gift banner.

## Source

- `dist/index.html`: page structure and dialog shells.
- `dist/styles.css`: desktop/mobile styling and reduced-motion support.
- `dist/app.js`: showroom navigation, search, category filtering, sorting, product dialogs, local cart and selection export.
- `dist/products.js`: editable sample catalogue with 17 models.
- `dist/assets/`: supplied logo, local fonts and reference catalogue imagery.
- `.openai/hosting.json`: static hosting configuration.

No dependency installation or build step is required. Serve `dist/` with a static HTTP server. The home page and collection/product views use hash routes.

## Current behavior

The showroom supports arrows, dots, keyboard arrows and horizontal swipes. Search matches model names and scales. Product details allow quantities from 1 to 99. The cart supports adding, quantity changes, removal and a text download. Cart state is persisted on the current browser/device. Native dialogs provide keyboard focus containment and Escape dismissal.

This is a private design preview. Prices and products are sample content from the reference, not confirmed DRMZ stock. RC products have not been supplied, so the RC view has an explicit coming-soon state. Checkout, payments, accounts and order processing are not connected. Contact, shipping and return information must be supplied before commercial launch. The preview does not collect personal or payment data or send cart state to a server.

## Assets

Brand logo: supplied by the user. Sample car photographs and cutouts: the user-selected reference https://toykoo.in/ (retrieved 18 November 2026). Original asset watermarks have not been altered. Fonts: Anton and DM Sans from Google Fonts. All runtime assets are local; no Shopify scripts, trackers or original shop checkout URLs are used.

## Validation

JavaScript syntax checked with `node --check`. Browser checks completed for desktop and a 390-pixel mobile viewport: showroom changes, model dialog, quantity selection, cart totals and persistence, search, collection filtering/sorting, mobile navigation and RC empty state. Loaded-image and horizontal-overflow checks passed on the inspected desktop view. Payment and order handling are intentionally unavailable.
