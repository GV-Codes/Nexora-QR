# FormaQR — Shape QR Studio

Static HTML/CSS/JavaScript QR design studio for GitHub + Vercel.

## Features
- 19 silhouettes across five categories: General, Flowers, Basic Shapes, Symbols & Nature, and Vehicles
- Short text accepts up to 5 alphanumeric characters (A–Z, 0–9); complete HTTP/HTTPS URLs can be longer; live preview updates as you type and over-limit text is flagged
- Square, rounded, and dot modules
- Center logo upload and custom silhouette image upload
- PNG and SVG downloads
- Responsive dark creative-studio interface
- No backend, login, database, or paid AI API required
- Images are read in the browser and not uploaded to a server

## QR library
The app loads the open-source `qrcode-generator` browser build from jsDelivr (MIT license). There is no paid API or backend. A network connection is required for the QR library to load. For fully offline use, download the library and serve it locally instead.

## Run locally
Run `python3 -m http.server 5500` from this folder, then open http://localhost:5500.

## Deploy with GitHub + Vercel
1. Create a GitHub repository named `formaqr-shape-studio`.
2. Upload all project files. The QR library is loaded from a free CDN.
3. Open Vercel and choose Add New → Project.
4. Import the GitHub repository.
5. Framework preset: Other.
6. Build command: leave empty. Output directory: `.` (project root).
7. Deploy and test URL entry, all shapes, logo upload, colors, PNG/SVG export, and phone scanning.

## Scan reliability
Scan-safe mode preserves the complete QR matrix and draws the chosen silhouette as a decorative outline. Artistic mode masks modules to a silhouette and can break decoding. Keep high contrast, preserve the quiet zone, keep center logos small, and scan-test all downloads before publishing.

## Current custom-image behavior
Center logo uploads are embedded in exported SVG/PNG. Custom silhouette uploads are accepted and kept local; in this starter version the selected built-in silhouette still controls the mask. Full alpha-aware arbitrary-image masking would require an additional mask-processing implementation.

## Portfolio summary
FormaQR is a responsive browser-based QR design studio with shape selection, color customization, image upload, QR module styling, and PNG/SVG export, designed for static deployment on GitHub Pages or Vercel.


### Shape categories
The shape picker is grouped into General (house, tree, coffee mug), Flowers (rose, tulip), Basic shapes (circle, rectangle, diamond, heart, square, star, hexagon), Symbols & nature (spade, clover, butterfly, cloud), and Vehicles (car, rocket, bicycle). Select a category tab to filter the shape tiles.
