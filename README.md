# app.quotiflex.com redirect

While the Quotiflex app server is switched off, app.quotiflex.com is served from this repository by GitHub Pages. Every address on it (index.html, and 404.html for any other path) sends the visitor to the contact form at https://quotiflex.com/#contact.

DNS at GoDaddy (quotiflex.com) while this is in use: `app` CNAME `teodorrohub.github.io` (set 2026-11-14).

Before that, `app` was delegated to AWS Route 53 with four NS records at GoDaddy:

- `app` NS `ns-1003.awsdns-61.net`
- `app` NS `ns-115.awsdns-14.com`
- `app` NS `ns-1298.awsdns-34.org`
- `app` NS `ns-1863.awsdns-40.co.uk`

The Route 53 zone `app.quotiflex.com` holds the server's address: `app.quotiflex.com` A `63.189.121.227`.

When the app server is back: in GoDaddy, delete the `app` CNAME and add the four NS records above again (TTL 1 hour). Then remove the custom domain in this repository's Pages settings, or delete the repository.
