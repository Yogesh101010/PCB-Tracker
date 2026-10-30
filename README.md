# PCB Build Tracker

Tracks every PCB from bare board to tested, and every project to fully tested pieces.

**Live view:** https://yogesh101010.github.io/PCB-Tracker/ (read only for everyone, works in any browser)

## What's in this repo

| Path | What it is |
| --- | --- |
| `index.html` | The tracker app |
| `pcbs/` | One Excel file per PCB |
| `projects/` | One Excel file per project |
| `Summary.xlsx` | Every PCB and project in one workbook, rewritten on each save |
| `files.json` | List of the Excel files, so the website knows what to load. Written by the app; don't edit by hand |
| `xlsx.full.min.js` | Excel reader/writer used by the app |

## Becoming the editor (one time)

1. Sign in to GitHub with an account that can push to this repository.
2. Create a token:
   - **You own the repository:** [New fine-grained token](https://github.com/settings/personal-access-tokens/new). Repository access: *Only select repositories* → this repo. Permissions: *Contents* → *Read and write*. Pick an expiry.
   - **You are a collaborator on someone else's personal repository:** fine-grained tokens can't reach it, so make a [classic token](https://github.com/settings/tokens/new?scopes=public_repo&description=PCB%20Tracker) with only *public_repo* ticked.
3. Open the live site, click **Editor sign in**, check the repository name, paste the token.

The token is stored only in that browser. Click **Sign out** to remove it, and revoke it on GitHub if a device is lost.

## How edits are published

Each save is kept in the editor's browser first. Everything waiting is sent to GitHub as **one commit**, either a set time after the last save or when the editor clicks **Publish now**. Choose the timing in the editor bar:

- Publish after each save
- 1 min after the last save (default)
- 5 min after the last save
- Only when I click

Viewers see the change once GitHub Pages redeploys, usually within a minute or two.

## Offline / without GitHub

Open `index.html` from a local copy in Chrome or Edge and pick the folder that holds it. Saves go straight into `pcbs/` and `projects/` there; commit and push to publish.
