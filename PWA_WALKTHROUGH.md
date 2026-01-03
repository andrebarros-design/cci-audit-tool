# PWA Conversion Walkthrough

This document outlines the changes made to convert the CCI Audit Tool into a Progressive Web App (PWA).

## 1. Directory Structure Changes

Two new files were added to the root directory `C:\Users\thean\Documents\Development\CCI\`:

-   **`manifest.json`**: This file contains metadata describing the app (Name, Icons, Start URL, etc.) allowing it to be installed on devices.
-   **`sw.js`**: A Service Worker script that caches the application assets (HTML, CSS, Fonts, Icons) to allow the app to work offline.
-   **Icons**: `icon-192.png` and `icon-512.png` were generated and saved to the root.

## 2. File Updates

### `index.html`

-   **Manifest Link**: Added `<link rel="manifest" href="manifest.json">` to the `<head>` section.
-   **Service Worker Registration**: Added a script at the end of the `<body>` to register the service worker:
    ```javascript
    if ('serviceWorker' in navigator) {
        window.addEventListener('load', () => {
            navigator.serviceWorker.register('sw.js', { scope: './' })
                .then(registration => console.log('SW Registered', registration))
                .catch(err => console.log('SW Failed', err));
        });
    }
    ```

### `manifest.json` configuration

-   **Start URL**: Set to `/cci-audit-tool/` to ensure compatibility with GitHub Pages hosting (e.g., `username.github.io/cci-audit-tool/`).
-   **Display**: Set to `standalone` to look like a native app (no browser bar).
-   **Theme Color**: Set to Teal (`#0d9488`) to match the app's brand.

### `sw.js` (Service Worker)

-   **Strategy**: "Cache-First". The app will try to load resources from the cache first for speed and offline access.
-   **Cached Assets**:
    -   `./` (Root)
    -   `./index.html`
    -   `./icon-192.png`
    -   `./icon-512.png`
    -   `https://cdn.tailwindcss.com` (External capability)
    -   `https://fonts.googleapis.com/css2?family=Inter...`

## 3. Verification

The app was served locally, and the Service Worker successfully registered (`SW Registered` in console). The manifest file is reachable and valid.

## Next Steps for Deployment

1.  **GitHub Pages**: Push these changes to your repository.
2.  Enable GitHub Pages in Settings -> Pages -> Source: `main` branch.
3.  The app will be installable from `https://your-username.github.io/cci-audit-tool/`.
