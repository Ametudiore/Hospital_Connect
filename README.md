# Hospital Connect

A responsive hospital discovery website with a Vite-powered, vanilla JavaScript frontend.

## Develop

Requires Node.js 20.19+ or 22.12+ (validated with Node.js 24).

```sh
npm ci
npm run dev
```

## Production build

```sh
npm run build
npm run preview
```

Deploy the generated `dist/` directory to a static web host.

## Features

- Live hospital-name and service search, area and ownership filters.
- Geolocation-based distance sorting (requires location permission and a secure browser context).
- Grid and grouped-by-area results; hospital profile dialogs.
- Saved hospital shortlist persisted in browser localStorage.
- Hospital subscription plans and a locally saved provider interest form.
- Responsive navigation and layouts, keyboard-accessible native dialogs.

## Demo boundaries

All six hospital listings are fictional examples in Lagos. Original bundled SVG illustrations do not depict real providers. DM Sans and Manrope fonts are bundled locally under their included SIL Open Font Licenses. The interface requires no third-party image or font requests.

Hospital subscription pricing is illustrative. The interest form stores data on the current device only and offers deletion; it does not submit information to a server. There is no authentication, payment processing, shared database, real provider verification, live appointment system, or production contact information. These integrations and verified hospital data are required before a public service launch.

## Validation

Production build and Chromium browser checks passed for search, no-results recovery, all filters, saved-state persistence, profile dialogs, geolocation sorting, grouped results, local subscription interest storage/deletion, mobile navigation, and mobile horizontal overflow. No browser JavaScript errors were observed.

## Publish with GitHub Pages

1. Push the project files to the `main` branch of `Ametudiore/Hospital_Connect`.
2. In the repository's **Settings → Pages**, select **GitHub Actions** as the source.
3. In **Actions**, run **Deploy Hospital Connect**, or push a change to `main`.
4. Open the website address shown in the successful deployment. For the standard project URL, this is `https://ametudiore.github.io/Hospital_Connect/`.

The workflow builds with the GitHub Pages base path so bundled images and fonts load correctly. Subsequent pushes to `main` update the site automatically. GitHub Pages must be available for the repository's visibility and account plan.

## Publish with Vercel

Import this repository into Vercel, select **Vite**, use `npm run build` as the build command and `dist` as the output directory, and deploy. The default root-path build supports Vercel without additional configuration.
