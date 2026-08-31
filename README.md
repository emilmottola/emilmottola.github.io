# emilmottola.com

Source for Emil Mottola’s public site (gravastars).

- Preview: https://emilmottola.github.io/ (`main` on GitHub Pages)
- Production: https://emilmottola.com/ (Namecheap / tesstech Stellar)

`main` is the source of truth. Pages updates itself on every push. Namecheap only updates when you hit **Actions → Deploy to Namecheap → Run workflow**.

## Ship to Namecheap

FTP secrets are already in the repo (repository secrets, not environment secrets). To go live:

1. Check https://emilmottola.github.io/
2. **Actions → Deploy to Namecheap → Run workflow** (branch `main`)

Do not put FTP credentials in the repo. Do not point a GitHub Pages custom-domain CNAME at emilmottola.com while Namecheap is serving it.
