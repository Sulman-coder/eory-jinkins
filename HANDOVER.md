# Rory Jenkins portfolio — local update, 15 November 2026

The editable website is in this directory. No build step or paid editor is required.
Open `index.html` to review it, or serve the folder with `python -m http.server 8080`.

## Client requirements and status

| Requirement | Status |
| --- | --- |
| Use only three clear, readable fonts | Complete: Montserrat for main headings/navigation, Poppins for body/controls, Playfair Display for section headings/editorial accents. Font files and SIL Open Font Licenses are included. Artwork and the supplied logo can contain their own lettering. |
| Correct wording | Corrected the obvious “Bill Board” typo, two artwork descriptions that did not match the displayed illustrations, and misleading contact button wording. The client's exact replacement copy was not included in the request and remains pending. |
| Add two illustrations and their thumbnails | Pending receipt/identification of the two approved originals, matching thumbnails, titles, descriptions and preferred order. Existing artwork is preserved. Do not assume that unused images are the approved additions. |
| Balance the layout | Complete in local code: consistent illustration columns, centred artwork, uncropped images, improved mobile sizing, readable paragraph widths and natural word spacing. English paragraphs remain left aligned; there is no need to move all text to the right. |
| Provide a complete ZIP | `artifacts/rory-jenkins-updated.zip` contains the updated HTML, CSS, JavaScript, all supplied images, resume PDF, local fonts, Bootstrap and their licenses. `artifacts/rory-jenkins-original.zip` preserves the original supplied files. |
| Hosting, Wix domain and administrative access | Pending account access and chosen hosting destination. No live deployment or DNS changes have been made. |

## Editing and adding the missing artwork

Edit page text in its corresponding `.html` file. Shared colours, font roles and responsive layout are in `css/style.css`; font faces are in `css/fonts.css`; behaviour is in `js/main.js`.

When the client provides the two new works, put their originals and matching thumbnails in `img/`. Add a `col-md-6 col-lg-4` block to `.illustration-grid` in `illustrations.html`. Use the thumbnail as the image `src`, and the full original as `data-lightbox`. Provide accurate `alt`, `data-alt`, `data-caption` and visible `figcaption` text. Keep intrinsic width/height attributes consistent with the actual image. Some existing `-sm` assets show different artwork from their similarly named originals; verify the pairing visually before using them.

## Contact behaviour

The form validates required name, email and message fields, then opens an email draft addressed to `jenkins_rory@yahoo.com`. Visitors must send that draft in their own email app. It has no server-side delivery service or inbox integration. Direct email and phone links remain available. End-to-end email delivery has not been tested.

## Hosting handover

1. Use a hosting account owned by the client and upload the ZIP contents with `index.html` at the website root. Keep the relative asset paths intact. No database or application runtime is needed.
2. Review the temporary hosting URL before changing the domain. Check every project, full-size artwork, menu, mobile layout, resume and email draft behaviour.
3. Obtain the exact domain records from the chosen host. If the domain is registered at Wix, it can point to external hosting using the host's required A/CNAME records. See [Wix's official external-site connection guide](https://support.wix.com/en/article/connecting-a-wix-domain-to-an-external-site). Preserve existing mail-related DNS records.
4. Enable HTTPS and verify the bare and `www` domains. Keep the old hosting available until the new site has been checked.
5. Give the client ownership/admin access to hosting, domain/DNS, billing and source backups, with the next maintainer invited through the provider's normal account controls. This ZIP cannot grant access to those accounts.

This is a static HTML website. Connecting its domain does not make these files editable in the Wix visual editor. Asset ownership and transfer permission for the supplied artwork, logo and resume remain with their respective owners; no new artwork has been generated or substituted.

## Validation

See `artifacts/verification.txt` for the source and local HTTP checks. Browser QA covers representative pages and interactions; it is not a guarantee of every browser/device combination. New images, exact copy corrections and live hosting verification remain pending.
