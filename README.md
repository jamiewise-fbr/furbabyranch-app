# Furbaby Ranch app

The Furbaby Ranch mobile app. It is a single web page that people can add to their phone's home screen, so it needs no app store.

**Status: not yet online.** The app shows real adoptable pets from Shelterluv, through the pet feed in the Furbaby Ranch Apps Script project (`AppFeed.gs`). GitHub Pages has not been turned on yet.

## What's here

| File | What it is |
|---|---|
| `index.html` | The whole app: screens, styles and behavior |
| `manifest.webmanifest` | The app's name, colors and icons for the home screen |
| `sw.js` | Lets the app open on a weak signal once installed |
| `icons/` | The shield logo and home screen icons |

## Changing things

- **Links** (applications, donations, shop, social): edit the `LINKS` list near the bottom of `index.html`.
- **Pets**: these come from Shelterluv automatically and refresh about every 15 minutes, so add, edit or remove pets in Shelterluv, not here. `FEED_URL` near the bottom of `index.html` holds the feed address. If it is emptied, the app shows the `EXAMPLES` list and a "Draft preview" banner.
- **Fees and adoption steps**: in the "ADOPT" section of `index.html`.
- After any change, raise the version in `sw.js` (`fbr-app-v1` to `fbr-app-v2`, and so on) so phones pick up the update.

## Putting it online with GitHub Pages

1. In this repository, open **Settings**, then **Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
3. After a minute or two the app is live at the address GitHub shows on that page.

## Keep out of this repository

Never add API keys, tokens or passwords here, including the Shelterluv key. Anything in this repository can be read by anyone who opens the app. Keys stay in the Apps Script project's Script Properties.
