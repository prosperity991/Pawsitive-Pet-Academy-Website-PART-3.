# Pawsitive Pet Academy — Part 3 (Functionality and SEO)

Responsive multi-page student project for a proposed Durban pet-care and training academy. The site uses teal, warm orange, cream and charcoal branding.

## Pages
- `index.html` — Home
- `about.html` — About, FAQ accordion and image lightbox gallery
- `courses.html` — JavaScript-generated course catalogue with search and category filter
- `quote.html` — Course selection and discount calculator
- `enquiry.html` — Dedicated course/service enquiry form (different purpose from general contact)
- `contact.html` — General message form and interactive Leaflet/OpenStreetMap map

## Run locally
Extract the folder and open it using VS Code Live Server. The Leaflet map requires an internet connection. Gallery illustrations are local SVG files in `images/`.

## JavaScript functionality
- Responsive dropdown/mobile navigation with accessible expanded-state attributes.
- Course catalogue generated from a JavaScript data array; live keyword search, category filtering, result count and empty state.
- FAQ accordion using native HTML `details`/`summary`.
- Click-to-enlarge image gallery; close button, backdrop click and Escape-key support.
- Leaflet interactive map centred on Durban city centre (not a confirmed academy address).
- Quote calculator: 5% discount for two courses; 10% for three or more; no discount for one.
- Separate enquiry and contact forms with required fields, HTML constraints, JavaScript validation, phone format checks, accessible errors and status messages.
- Both forms support asynchronous submission using `fetch` and `FormData` when configured with a valid form service endpoint.

## Form delivery configuration — required before live submission
The forms currently validate locally; they do not deliver messages until connected to a real form endpoint. To enable delivery:
1. Create a form endpoint with a service such as Formspree or FormSubmit using an email address authorised by the project/business owner.
2. Verify the recipient address with that provider.
3. Replace the placeholder Formspree URL in both the `action` and `data-endpoint` attributes (`#enquiry-form` in `enquiry.html` and `#contact-form` in `contact.html`) with each form’s exact HTTPS endpoint. Use separate form endpoints if the provider requires them.
4. Keep `action` aligned with the endpoint if required by the chosen provider, and test a real submission from a deployed site.
5. Never put private API keys or passwords in browser JavaScript. Check spam filtering and privacy requirements.

## SEO implementation
- Page-specific titles, descriptions and relevant Durban/pet-care keywords.
- Semantic headings, internal links and descriptive image alternative text.
- Descriptive HTML page filenames and canonical URL placeholders.
- `robots.txt` and `sitemap.xml`, including all six pages.
- Local SVG gallery artwork with meaningful alt text and lazy loading.
- Local SEO suggestions: publish accurate approved address/phone/email details; if this is a real eligible business, create and verify a Google Business Profile.
- Off-page SEO: request relevant, genuine links from local animal welfare groups, veterinary practices, pet clubs and training partners; share useful content through official social accounts. Do not fabricate backlinks, reviews or social profiles.

## Performance and security
- Local SVG artwork avoids large third-party gallery downloads; gallery images are lazy-loaded.
- CSS/JS are shared across pages and JavaScript is deferred.
- `_headers` provides basic security response headers on Netlify. If hosting elsewhere, configure equivalent HTTPS/security headers at the host.
- Keep third-party libraries updated; use HTTPS; do not collect unnecessary personal information; do not publish real contact details without owner approval.
- Run Lighthouse/PageSpeed Insights after deployment and record actual performance/accessibility/SEO scores. No score is claimed here because no live deployment test has yet been run.

## Deployment and URL configuration
Before publishing, replace `YOUR-DEPLOYED-DOMAIN.example` in canonical tags, `robots.txt` and `sitemap.xml` with the actual HTTPS website URL. Deploy the folder to Netlify (or another free static host), then check all pages, forms and map on the live URL. Submit the sitemap in Google Search Console if appropriate.

## Part 2 feedback
The Part 2 lecturer feedback was not supplied with the source files. Add the exact lecturer comments and the corresponding changes here once received; no feedback-specific corrections are claimed without that evidence.

## Changelog — 2 November 2026
### Part 3
- Added dedicated `enquiry.html` with course/service enquiry fields, separate from the general contact form.
- Updated `contact.html` to explain its general-message purpose and link to the dedicated enquiry page.
- Added reusable client-side validation and optional asynchronous FormData submission for both forms, including name, email, message and phone validation and accessible feedback.
- Added three original local SVG gallery illustrations with descriptive filenames and alt text; updated lightbox to display the selected image.
- Updated shared navigation/footer links to include the enquiry page.
- Updated sitemap to include all six pages and retained robots/canonical placeholders for replacement after deployment.
- Added basic Netlify security response headers in `_headers`.
- Documented configuration steps for form delivery, SEO, deployment, page-speed testing and ethical off-page SEO.

## Testing checklist
- [ ] Open all six pages and test every navigation/footer link.
- [ ] Test mobile menu and Explore dropdown using mouse and keyboard.
- [ ] Search/filter courses and verify the result count and no-results state.
- [ ] Select one, two and three courses; verify quote totals and discount percentages.
- [ ] Test both forms with blank fields, invalid email, invalid phone and valid details.
- [ ] Configure a real verified form endpoint and test successful and failed network submissions.
- [ ] Open each gallery image; close with button, backdrop and Escape.
- [ ] Confirm map and tiles load while online; marker is only an area reference.
- [ ] Replace all domain placeholders and confirm sitemap/robots URLs.
- [ ] Deploy; run Lighthouse/PageSpeed Insights and record measured results.
- [ ] Push to GitHub with descriptive commits and submit repository and live-site URLs.
- [ ] Apply and document actual Part 2 feedback when received.

## References
- Google Search Central. (n.d.). *SEO Starter Guide*. https://developers.google.com/search/docs/fundamentals/seo-starter-guide
- Google Search Central. (n.d.). *Introduction to robots.txt*. https://developers.google.com/search/docs/crawling-indexing/robots/intro
- Google PageSpeed Insights. (n.d.). *About PageSpeed Insights*. https://developers.google.com/speed/docs/insights/v5/about
- MDN Web Docs. (n.d.). *Constraint validation*. https://developer.mozilla.org/en-US/docs/Web/HTML/Constraint_validation
- MDN Web Docs. (n.d.). *Fetch API*. https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API
- Leaflet. (n.d.). *Quick start guide*. https://leafletjs.com/examples/quick-start/
- OpenStreetMap. (n.d.). *Copyright and licence*. https://www.openstreetmap.org/copyright
- Sitemaps.org. (n.d.). *Sitemaps XML format*. https://www.sitemaps.org/protocol.html
- Netlify. (n.d.). *Custom headers*. https://docs.netlify.com/manage/routing/headers/
