# Gibbs Gunsmithing, LLC Website

A responsive, static website built from the wording and photographs in the supplied Gibbs Gunsmithing brochure.

## Files

- `index.html` — page content and site structure
- `styles.css` — layout, colors, typography, and responsive styling
- `script.js` — mobile navigation and current copyright year
- `assets/` — photographs and logo images extracted from the brochure
- `CNAME` — custom domain for GitHub Pages

## Preview locally

Open `index.html` in a browser. For a more reliable local preview, run a simple local web server from this folder:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Create or open the GitHub repository that will hold this website.
2. Upload the contents of this folder to the repository's publishing branch (commonly `main`) and place `index.html` at the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then save.
6. Wait for GitHub Pages to finish publishing.

## Connect `gibbsgunsmithingllc.com` through GoDaddy

The `CNAME` file is already included. In the repository's **Settings → Pages → Custom domain**, enter:

`gibbsgunsmithingllc.com`

Save, and wait for GitHub to verify the domain. Then open the domain's DNS management in GoDaddy and configure:

### Apex/root domain (`gibbsgunsmithingllc.com`)

Add these four **A** records (Host: `@`):

| Type | Host | Points to |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Add this **CNAME** record for `www`:

| Type | Host | Points to |
|---|---|---|
| CNAME | www | `tgibbs0318-max.github.io` |

If your GitHub username or Pages host is different, replace the CNAME destination with the host GitHub shows for your account. Remove conflicting `A`, `AAAA`, or `CNAME` records for `@` or `www` if they point elsewhere. Do not delete unrelated email/MX records.

Once DNS has propagated and GitHub verifies the domain, enable **Enforce HTTPS** in GitHub Pages settings. DNS changes can take some time to propagate.

## Updating the website

Edit `index.html` to change text, phone number, email, or address. Edit `styles.css` to change the appearance. Keep the `assets` folder in the same location so the image paths continue to work.

## Notes

- The brochure's listed phone number, email, address, services, and business descriptions have been carried into the site.
- The contact links open the visitor's phone or email app; this static website does not store or process contact-form submissions.
- The range is described as private and not open to the public, consistent with the brochure.
- Review all business details, service descriptions, and regulatory wording before publishing.
