# Goodlex Group Limited website

A responsive React 18 + Vite 6 corporate site with React Router and Lucide icons. It presents Goodlex as investing its own capital, not as a public fund, deposit taker or third-party fund manager.

## Run locally

Requires Node.js 20+ and npm.

```sh
npm install
npm run dev
```

For a production build run `npm run build`, then `npm run preview` to test it locally.

## Project structure and content updates

- `src/main.jsx`: shared header and footer, page content, navigation, industries and values. Edit the `industries`, `principles`, `values`, and `nav` arrays to update shared content; each page component contains its page-specific copy. Add only verified company and leadership details.
- `src/style.css`: all responsive styling, brand colours and breakpoints.
- `public/images/`: locally hosted WebP visual assets and the provisional screenshot logo crop.
- `index.html`: default title and description. Page titles and descriptions are set on navigation in `App`.

The industry images and hero/globe imagery are AI-generated illustrative visuals, not evidence of company holdings or locations. Replace them with properly licensed, approved assets if required. The only supplied logo is embedded in the visual reference screenshot. `logo-reference-crop.png` is a crop of that reference, not a verified original standalone logo. Replace it with the original client-provided GX logo file before launch; retain its proportions and update the image path in `Brand` if the filename changes.

## Deployment and HTTPS

1. Run `npm install`, `npm run build`, and verify `dist/` locally.
2. Deploy the contents of `dist/` to a static hosting provider (e.g. Netlify, Cloudflare Pages or Vercel). Configure a single-page-app rewrite so all paths return `/index.html` (Netlify's included `public/_redirects` does this automatically).
3. Connect the official domain through the hosting provider and update DNS records as directed by that provider. Enable automatic HTTPS/TLS and force HTTPS.
4. Verify the domain, certificate, every route and dropdown, mobile navigation, email link and images on real desktop and mobile devices. Confirm page titles and descriptions and submit a sitemap if desired.

Deployment and DNS require access to the domain and hosting account; they have not been performed in this workspace. No form, analytics, cookies or social media links are configured. The contact page uses a `mailto:` link. Page metadata is client-rendered; for maximum search indexing and social sharing, pre-render routes or migrate metadata to server-side rendering before launch. The Google Fonts stylesheet requires network access; system-font fallbacks are provided.
