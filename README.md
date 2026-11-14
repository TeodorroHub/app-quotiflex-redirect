# app.quotiflex.com redirect

While the Quotiflex app server is switched off, app.quotiflex.com is served from this repository by GitHub Pages. Every address on it (index.html, and 404.html for any other path) sends the visitor to the contact form at https://quotiflex.com/#contact.

DNS at GoDaddy while this is in use: `app` CNAME `teodorrohub.github.io`.

When the app server is back: in GoDaddy, delete the `app` CNAME and add back `app` A `63.189.121.227`; then remove the custom domain in this repository's Pages settings (or delete the repository).
