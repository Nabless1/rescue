# Nabless rescue tool

This repository holds one thing: copies of the page that lets a person use and
recover a Nabless Vault **without Nabless**. It exists so that a genuine copy
can still be found if nabless.com is ever unavailable.

It contains the built page only. It is not the source of the Nabless apps,
service or contracts.

## Status: pre-launch

- Nabless is **not launched**. This build knows **test networks only**. No
  real money is involved.
- Nabless has **not been independently audited** yet.
- This release is **not yet signed**. A signed release will follow; until
  then, treat the fingerprint below as the only check.

## Latest release

| Release | File | SHA-256 fingerprint |
| --- | --- | --- |
| 2026-11-25-r6 | `releases/2026-11-25-r6/nabless-rescue-2026-11-25-r6.zip` | `c1394024a0cd3293a8077c0e11d4daa1c0d11cfec62bbe3babc66673b1768cee` |

It knows Vaults made on contract revisions 1 to 6. Use the latest release: an
earlier one does not know Vaults made on a later revision.

## Earlier releases

| Release | File | SHA-256 fingerprint |
| --- | --- | --- |
| 2026-11-25-r5 | `releases/2026-11-25-r5/nabless-rescue-2026-11-25-r5.zip` | `1d6c8fc721a9f797839253301e132c753a38155238daeb5aceff4a16d255d50e` |

## How to use it

1. Download the zip and check its fingerprint:
   `shasum -a 256 nabless-rescue-2026-11-25-r6.zip`
   It must match the value above exactly.
2. Unzip it and serve the folder from your own computer, for example:
   `python3 -m http.server 8080` and open `http://localhost:8080/rescue/`.
   Opening the file straight from disk does not work: passkeys need a real address.
3. Follow `README.txt` inside the folder.

You will need the Vault file you saved from the app, and, to get back in with
a new passkey, your recovery kit and your backup key.

## Stay safe

- Only use a copy whose fingerprint you have checked.
- This page never asks for a seed phrase or a private key.
- A false copy cannot move your money without your approvals, but it could
  ask for your recovery kit, your backup key and their passwords. A hardware
  wallet as backup key never hands its key to any page.
