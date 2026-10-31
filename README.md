# Tracking App mobile site

This is a static mobile website version of the iPhone sales tracker. It has a dashboard, sales list, add/edit/delete, shipped status, totals, and JSON import/export. Records stay in the browser's local storage on the device where they were entered. It does not sync between devices or upload sales to the hosting provider.

## Host it

Upload the files in this folder to a static host such as GitHub Pages, Cloudflare Pages, Netlify, or your own web server. Serve them over HTTPS for offline support and Add to Home Screen. No build step or server-side code is required.

On iPhone, open the hosted URL in Safari, tap Share, then **Add to Home Screen**. The site can also be opened directly in a browser.

The site includes an iPhone Home Screen icon (`apple-touch-icon.png`) and an SVG browser/manifest icon. After deploying an icon change, remove an existing Home Screen shortcut and add it again to refresh the cached icon.

## Move records from the iPhone app

If the native app is still accessible, use its **Settings → Export Data** to save a JSON backup. In the hosted site, open **Settings → Import Data** and select that file. The web version reads the app's default JSON date format and exports the same format. Importing appends records, so avoid importing the same backup twice.

If the native app can no longer open, its records cannot be read by the website directly. Reinstall/sign it from Xcode first if possible, export a backup, then import it here.

Because records are stored locally in Safari, use **Export Data** regularly. Clearing Safari website data can remove them. For phone-to-phone syncing, a shared backend would need to be added.
