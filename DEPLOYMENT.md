# Dawn Patrol deployment

Production URL: https://surfdaddy.surf/dawnpatrol/

Repository: geekdecoder/surf-report-chatgpt (main)

## CyberPanel

1. Confirm `surfdaddy.surf` is configured as a website and HTTPS works.
2. In CyberPanel's file manager, find the document root for `surfdaddy.surf` (typically `/home/surfdaddy.surf/public_html`, but verify before using).
3. Create a `dawnpatrol` directory inside that document root.
4. Deploy `index.html`, `styles.css`, `app.js`, and the `reports/` directory into `dawnpatrol/`.
5. Verify https://surfdaddy.surf/dawnpatrol/ loads and the archive shows its initial empty state.

The site uses relative asset paths so it works under `/dawnpatrol/` without changing application code.

## Automation (not yet configured)

GitHub Actions deployment requires a limited SSH deploy key and repository secrets; never commit server passwords, SSH private keys, or API keys. Daily generation should finish before 06:00 America/Chicago, account for daylight saving time, and have failure alerts and a server-side fallback. Animated presenter videos require a separate rendering pipeline.
