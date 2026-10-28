# Update log

## 2026-10-28 — Sitemap publisher integration audit

- Added missing GA4 / GTM integrations to sitemap-listed static source pages. Existing AdSense and existing GA property IDs are preserved.
- Added guarded Cloudflare fallback and GTM noscript fallback. Existing Cloudflare edge beacons are reused; local preview hosts do not initialize the new integrations.
- Existing HTML, app scripts, styles, embedded documents and page content remain byte-for-byte unchanged outside the new marked integration blocks. These repositories serve static HTML directly and have no source generator requiring a rebuild.
- GA property used: `G-CV4YSSX8VK`. Changed HTML: `index.html`, `privacy/index.html`, `service/index.html`.

- Bumped the investment PWA cache version so returning users can receive the updated HTML. Cache lookup uses the app’s current cache; activation only removes old `invest-ai-` caches. No user data stores or other apps’ caches are cleared.
