# FormaQR — Shape QR Studio

Static HTML/CSS/JavaScript QR design studio for GitHub + Vercel.

## Features
- 25 original silhouette options across six categories: General, Flowers, Basic Shapes, Symbols & Nature, Vehicles, and Cartoon
- Cartoon-inspired silhouette concepts: Cat & Mouse, Cheerful Mouse, Playful Duck, Chipmunk Duo, Flying Elephant, and Lion Cub; these are generic original shapes, not official character artwork
- Short text accepts up to 5 alphanumeric characters (A–Z, 0–9); complete HTTP/HTTPS URLs can be longer
- Live preview and clear validation feedback while entering text
- Square, rounded, and dot QR modules
- Foreground/background color controls and preset palettes
- Center logo upload and custom silhouette image upload
- PNG and SVG downloads
- Responsive dark creative-studio interface
- No backend, login, database, or paid AI API required
- Images are read in the browser and not uploaded to a server

## Cartoon artwork and licensing
The Cartoon category uses simple, original cartoon-inspired geometric silhouettes drawn in code. It does not include official Tom and Jerry, Mickey Mouse, Donald Duck, Chip and Dale, Dumbo, or Simba artwork and is not affiliated with their rights holders. If you add Creative Commons artwork later, verify the license on the original source, keep the creator/license attribution where required, and check whether commercial use and adaptations are allowed. Avoid using a character's name or branding in a way that implies endorsement.

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
7. Deploy and test text entry, URLs, categories, logo upload, colors, PNG/SVG export, and phone scanning.

## Scan reliability
Scan-safe mode is enabled by default and preserves the complete QR data grid while drawing the chosen silhouette as a decorative outline. Artistic mode masks modules to a silhouette and can break decoding. Keep strong foreground/background contrast, preserve the quiet zone, keep center logos small, and scan-test every exported file with multiple phone cameras before publishing. Visual styling alone cannot guarantee scan reliability across all devices and print sizes.

## Current custom-image behavior
Center logo uploads are embedded in exported SVG/PNG. Custom silhouette uploads are accepted and kept local; in this starter version the selected built-in silhouette still controls the mask. Full alpha-aware arbitrary-image masking would require an additional mask-processing implementation.

## Portfolio summary
FormaQR is a responsive, browser-based QR design studio with short alphanumeric text and full URL support, six silhouette categories including original cartoon-inspired designs, color and module customization, local image upload, live preview, and PNG/SVG export. It is designed for static deployment on GitHub Pages or Vercel.
