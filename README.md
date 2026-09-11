# Corridor Sweep

A password-gated research note on twelve months of acquisitions and investments in
cross-border payment infrastructure by stablecoin issuers and card networks.

The published page is encrypted. `index.html` contains ciphertext only — the content
cannot be read from page source without the password.

## Structure

| File | Published | Notes |
|---|---|---|
| `index.source.html` | No — gitignored | Plaintext source. Edit this. |
| `index.html` | Yes | Encrypted build. Generated, do not edit by hand. |
| `encrypt.js` | Yes | Build script. AES-256-GCM, PBKDF2-SHA256, 250k iterations. |

## Rebuilding after an edit

Edit `index.source.html`, then:

```bash
NTB_PASSWORD='<password>' node encrypt.js --in index.source.html --out index.html --label "Corridor Sweep"
```

Commit the regenerated `index.html` and push. The password is never written into any
committed file and is not recorded in this repo.

## Publishing

`index.html` serves from GitHub Pages on the `main` branch. Pushing redeploys.

## Sourcing conventions

Claims in the note carry a confidence marker and a link to the source behind them:

- **Verified** — confirmed against a primary source (a company filing or investor
  release) or corroborated across multiple independent outlets.
- **Reported** — secondary coverage only. Re-check against primary sources before
  relying on it.

Market-sizing and adoption figures come from trade coverage and industry surveys rather
than official statistics, and are flagged as directional on the page itself.
