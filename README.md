# emilmottola.com

Source for Emil Mottola’s public site (gravastars).

- Preview: https://emilmottola.github.io/
- Production: http://emilmottola.com/ (Namecheap / tesstech Stellar)

`main` is the source of truth. GitHub Pages updates itself. Namecheap updates when the Deploy to Namecheap Action succeeds (FTPS into the addon folder).

## Ship to Namecheap

One-time, from a browser on a stable IP (not this sandbox):

1. cPanel → **FTP Accounts** → add a user whose directory is `/home/tesscrri/emilmottola.com` (not `public_html`).
2. GitHub repo → **Settings → Secrets and variables → Actions**, add:
   - `FTP_SERVER` — `server293.web-hosting.com` (or whatever cPanel shows as FTP host)
   - `FTP_USERNAME` — the FTP account, often `something@emilmottola.com`
   - `FTP_PASSWORD` — that account’s password
3. Push to `main`, or **Actions → Deploy to Namecheap → Run workflow**.

Until those secrets exist the job is skipped, so preview still works.

Do not put FTP credentials in the repo. Do not point a GitHub Pages custom-domain CNAME at emilmottola.com while Namecheap is serving it.
