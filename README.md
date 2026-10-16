# Apoorva Info Lab - static website

Plain HTML, CSS and JavaScript. No Node.js needed.

Upload the contents of this folder to the root of any web host (Apache, Nginx, cPanel, GitHub Pages, Netlify).
Each page lives in its own folder (about/index.html, products/aims/index.html ...).

To preview locally: run `python3 -m http.server` inside this folder, then open http://localhost:8000.
The site must be served from the domain root by a web server (not opened by double-clicking files).

The demo form opens the visitor's email app with a pre-filled message to mkt@apoorva.info.

## Hosting on cPanel (secure setup)

1. cPanel → SSL/TLS Status → Run AutoSSL (free HTTPS certificate).
2. File Manager → public_html → Upload the ZIP → Extract, so index.html sits directly in public_html.
3. Settings → tick "Show Hidden Files" and check that `.htaccess` is present.
4. Visit your site, then test it at https://securityheaders.com.

The `.htaccess` file forces HTTPS, removes www, adds security headers (CSP, HSTS, anti-framing, nosniff),
hides folder listings, blocks hidden/backup files, sets caching and compression, and shows 404.html for missing pages.
