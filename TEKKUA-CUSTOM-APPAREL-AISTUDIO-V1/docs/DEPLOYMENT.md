# Deployment

1. `npm test && npm run build`
2. Upload this Git repository to GitHub. Do not strip `src/images.js`.
3. Import to Google AI Studio (validate image rendering and module behavior inside Studio; not yet tested).
4. For Cloudflare Pages static hosting, set build command `npm run build` and output directory `dist`.
5. Before any real customer use, replace placeholder TEKKUA business identity if needed, sample photos, contact details, and remove unverified content. Configure actual direct WhatsApp in `src/data.js`.
6. All routes return `index.html` via the included `_redirects` file.
