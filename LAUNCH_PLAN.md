# Linea Lab Website Refresh — Launch Plan

**Metadata**
- **Status:** Working
- **Last updated:** June 24, 2026
- **Owner:** David / Brandon / Emery
- **Update trigger:** Update when the launch domain, deployment method, contact flow, or final asset set changes.
- **Generated:** yes

This is the launch note for the current sparse The Studio Deux-style Linea Lab website refresh. David confirmed on June 24, 2026 that this clean sister-site version is the refresh version to keep. The active site files live in this folder and can be deployed as a static site: `index.html`, `styles.css`, `script.js`, and the `assets/` folder.

## Recommended Launch Path

Use **Cloudflare Pages Direct Upload** for the first launch. This avoids the private repo media-exclusion issue: the Studio Deux repo intentionally ignores raster image files, while this site needs local image assets such as the Linea Lab mark and team portraits.

Cloudflare Pages Direct Upload supports uploading a single folder or zip of prebuilt static assets from the dashboard. The upload should include the contents of:

`07_APPS/Linea Lab Website Refresh/`

Not just the HTML file.

## Dashboard Steps

1. Open Cloudflare Dashboard.
2. Go to **Workers & Pages**.
3. Choose **Create application**.
4. Choose **Pages** / **Direct Upload** / **Drag and drop your files**.
5. Create a project, for example: `linea-lab`.
6. Upload the full refresh folder, including:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `assets/`
7. Deploy and check the temporary `*.pages.dev` URL.
8. In the Pages project, go to **Custom domains**.
9. Add the launch domain, likely `linealab.ai` and/or `www.linealab.ai`.
10. Because the domain is already hosted in Cloudflare, Cloudflare should be able to create or guide the needed DNS record from the custom-domain setup flow.

## Important Pre-Launch Checks

- Confirm whether the public URL should be `linealab.ai`, `www.linealab.ai`, or both.
- Confirm the Adobe Fonts / Typekit kit allows the final Linea Lab domain, otherwise Orpheus Pro and Adobe Garamond Pro may not load on the live site.
- Current contact flow is a simple `mailto:` contact form using `hello@linealab.ai`. Swap to a real approved booking/form flow later if the team wants lower-friction scheduling.
- Review copy once more for David / Brandon / Emery names, service order, and final email address.
- Test desktop and mobile after deployment.

## Useful Source Docs

- Cloudflare Pages Direct Upload: https://developers.cloudflare.com/pages/get-started/direct-upload/
- Cloudflare Pages Custom Domains: https://developers.cloudflare.com/pages/configuration/custom-domains/
