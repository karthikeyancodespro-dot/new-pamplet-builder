# Supermarket Pamphlet Builder - deploy package

`index.html` is the **whole app in one file** (design + code inside it). Nothing else is needed for it to work, so it cannot lose its styling or scripts because of a wrong folder or URL.

## Deploy on Vercel (free)
**A. GitHub (no installs)**
1. Unzip this package and create a new GitHub repository.
2. Upload the **files inside** the unzipped folder (`index.html`, `vercel.json`, `manifest.webmanifest`, `icons`, ...) so `index.html` is at the very top of the repository, not inside another folder.
3. On vercel.com: **Add New > Project**, import the repository, **Framework Preset = Other**, **Root Directory = ./**, leave Build/Output empty, click **Deploy**.

**B. Vercel CLI**
```
npm i -g vercel
cd <the unzipped folder>
vercel --prod
```
**C. Netlify Drop (fastest):** drag the unzipped folder onto https://app.netlify.com/drop

## After you redeploy
Open the site and press **Ctrl+Shift+R** (phone: reload / clear site data). This version also clears any old cached app files by itself. Your saved pamphlets stay in the browser.

## Watermark (brand logo behind the pamphlet)
Click **💧 Watermark** (above the preview) to open the Watermark Studio: choose your logo, pick Subtle / Classic / Bold, and adjust opacity, size, position (or repeat), layer, logo colors (original / blue tone / grayscale) and "remove white background". A live preview of page 1 updates as you change settings. It appears only in the preview and in downloads / print, never in the editor.

## Product image formats
JPG, JPEG, JFIF, PNG, APNG, GIF, WebP, AVIF, BMP, ICO, SVG work directly. TIFF and HEIC/HEIF are converted automatically (a small helper is loaded from jsDelivr the first time). DICOM (.dcm) works for uncompressed files; compressed DICOM must be exported as JPG/PNG first.

## Files
```
index.html                      the complete app (deploy this)
vercel.json                     tells Vercel not to cache old copies
manifest.webmanifest + icons/   "Add to Home screen" support (optional)
source/                         readable split version (css/styles.css, js/app.js) - NOT needed to deploy
CHANGELOG.md                    everything built so far
```
Needs internet for Google Fonts and the export libraries (cdnjs, with jsDelivr as backup).

## Shortcuts
Ctrl+Z undo - Ctrl+Y redo - Ctrl+S save project - Arrow keys move between cells (Ctrl+Arrow = edge) - Enter next row (Product Name: Enter = new line, Ctrl+Enter = next row) - Shift+Enter previous row - Ctrl+D fill down - F2 edit cell - paste cells from Excel / Google Sheets.
