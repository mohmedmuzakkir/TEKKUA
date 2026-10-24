# TEKKUA Custom Apparel — AI Studio Safe Sample V1

An animated, mobile-responsive apparel showcase SPA made from the approved desktop/mobile visual mockups. **This is an independent sample, not a modification of MUZA AgencyOS V5:** the original AgencyOS ZIP was not available during generation. Brand TEKKUA is a **temporary sample name**. Images are cropped/processed from the supplied conceptual mockups, not verified product photographs. Product prices, WhatsApp number, real testimonials, delivery commitments, and stock data are intentionally not invented.

## Run / build / test

Requirements: Node.js 18+. No third-party runtime packages or npm installation required.

```
npm run dev
npm run build
npm test
npm run preview
```

Open http://localhost:4173. Static build output: `dist/`. Deploy dist to Cloudflare Pages; `_redirects` provides SPA routing. GitHub → Google AI Studio: import the full repository, and preserve the `src/images.js` data URI module. This convention is intended to avoid missing binary images, but has **not yet been verified within Google AI Studio**.

## Image strategy

Images embedded in `src/images.js` as base64 WEBP data URIs. All UI assets are loaded via `const img = n => IMAGES[n] || '/assets/' + n + '.webp';` inside `src/app.js`. The assets folder exists only as fallback. No silent broken-image masking. No external image URLs are needed. Google Fonts are optional; system fallbacks work when offline.

## Pages

Home / Shop / Product Details / Customize / Bulk Orders / Our Work / About / Contact. Animated slider, scroll reveal, category filtering, product searches, size/color/quantity selection, localStorage demo favorites & shopping bag, upload-and-preview artwork, enquiry composition. Contact form creates an enquiry in-browser; it does not submit to a server. Facebook link is included. Set real WhatsApp number in `src/data.js` later (without `+`, country code included) to enable direct WhatsApp inquiries.

## Restrictions

No account authentication, server-side admin, stock, payment processing, database or real product management included. Shopping bag is browser-local only. File uploads remain local and are not transmitted. For any production rollout: obtain client branding, real photos and permission, pricing, policies, validated content, contact information, secure backend and appropriate security review.

## File changes

New standalone project. `src/app.js` pages and interactions; `src/style.css` design and animations; `src/images.js` base64 images; `src/data.js` product sample records; scripts and tests for build verification. Existing AgencyOS sources/functions have not been edited or retained, since the source ZIP is absent.
