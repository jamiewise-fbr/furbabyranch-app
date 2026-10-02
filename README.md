# Furbaby Ranch app

The Furbaby Ranch mobile app. It is a single web page that people can add to their phone's home screen, so it needs no app store.

**Live at https://app.furbabyranch.com** (hosted with GitHub Pages from the `main` branch). The app shows real adoptable pets from Shelterluv, through the pet feed in the Furbaby Ranch Apps Script project (`AppFeed.gs`).

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

## Publishing changes

GitHub Pages is on, so any change committed to the `main` branch goes live within a minute or two. To take the app offline, open **Settings**, then **Pages**, and set the branch to **None**.

The `app.furbabyranch.com` address works through two settings: a CNAME record named `app` pointing to `jamiewise-fbr.github.io` in the domain's DNS (Squarespace Domains), and the custom domain in this repository's Pages settings, which GitHub stores in the `CNAME` file here. Leave that file in place.

## Keep out of this repository

Never add API keys, tokens or passwords here, including the Shelterluv key. Anything in this repository can be read by anyone who opens the app. Keys stay in the Apps Script project's Script Properties.
