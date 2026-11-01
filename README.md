# BrightPath Youth Development Foundation – Website Project

## 1. Student Information
- Student name: Fana Thopola
- Student number: ST10473433
- Subject: WEB DEVELOPMENT
- Subject code: WEBDE5020

## 2. Links
- GitHub repository: (https://github.com/Quellivy11/BrightPath.git)


## 3. Project Overview
BrightPath Youth Development Foundation is a fictional non-profit organisation that I created for this academic website project. The organisation focuses on youth development, digital skills, career readiness and mentorship in Polokwane and Seshego, Limpopo.

The website gives visitors information about the organisation and its programmes, and clear ways to volunteer, sponsor activities or make general enquiries.

## 4. Website Goals and Objectives
1. Establish a clear and professional online presence for the organisation.
2. Explain the organisation's mission, vision and programmes.
3. Provide clear calls to action for volunteering and sponsorship.
4. Make contact and enquiry information easy to find.
5. Create a responsive website that is usable on desktop and mobile devices.
6. Make the website easy for search engines to understand and for people to find (Part 2).

## 5. Key Features and Functionality
- Responsive five-page website (plus a custom 404 page).
- Consistent navigation, skip link and footer across all pages.
- Home, About Us, Programmes, Enquiry and Contact pages.
- Volunteer, sponsor and programme enquiry options.
- JavaScript form validation, enquiry pre-fill, live "Open now" badges and an animated statistic (see section 7).
- Two fictional contact locations with embedded maps.
- Semantic HTML, accessible form labels and visible keyboard focus.
- On-page SEO, `robots.txt` and `sitemap.xml` (see section 6).

---

## 6. Part 2 – How I applied the SEO and Publishing guide

I worked through the *Student SEO and Publishing Guide*, which uses a bakery website as its example, and applied every step to BrightPath instead. Where the guide talks about "cakes in Polokwane", I used the equivalent for my organisation, such as "youth programmes in Polokwane".

### 6.1 Choosing search phrases
I thought about what a real person in Limpopo might type into a search engine and picked one honest phrase per page:

| Page | Search phrase I targeted |
|---|---|
| `index.html` | youth development programmes in Polokwane |
| `about.html` | BrightPath Youth Development Foundation Limpopo |
| `services.html` | youth skills and career programmes in Polokwane |
| `enquiry.html` | volunteer / sponsor / join a youth programme |
| `contact.html` | BrightPath contact details Polokwane and Seshego |

I worked these phrases into the titles, descriptions and main headings naturally, without repeating them over and over.

### 6.2 Unique titles and meta descriptions
Before, some titles were very short (for example "Contact | BrightPath"). I rewrote every `<title>` and `<meta name="description">` so each page has its own accurate summary of 50–160 characters. I also added Open Graph tags (`og:title`, `og:description`, `og:site_name`) so pages show a proper preview when shared on social media or WhatsApp, a `theme-color` and a small SVG favicon.

### 6.3 Heading structure
I checked that each page has exactly one `<h1>`, with `<h2>` for major sections and `<h3>` for subsections:
- On the About page, the Mission/Vision/Values cards used `<h2>` without a section heading. I added an `<h2>` "Our mission, vision and values" and turned the cards into `<h3>`s.
- The footer headings ("Explore", "Locations") were `<h3>`s with no parent section, so I changed them to `<h2 class="footer-heading">`.
- I changed the "Learn → practise → apply" steps into an ordered list (`<ol>`) because they are a sequence.

### 6.4 Descriptive images and alt text
- I renamed the images from names like `Lebo Mokoena.jpeg` (with spaces) to descriptive, lower-case, hyphenated names such as `lebo-mokoena-programme-coordinator.webp` and `youth-group-digital-skills-workshop.webp`.
- I rewrote the alt text to describe the image, e.g. *"Portrait of Lebo Mokoena, BrightPath Programme Coordinator, wearing a brown suit"*, instead of just the name.
- Decorative items (the "BP" logo mark and the 01/02/03 numbers) are hidden from screen readers with `aria-hidden="true"`.

### 6.5 Descriptive links and internal linking
- I replaced the three identical "View programme →" links on the home page with links that say where they go, such as "Explore the Career Ready programme →". These now jump straight to that programme using anchors (`services.html#career-ready`).
- Each programme on the Programmes page now ends with a link like "Enquire about joining Career Ready →", so related pages link to one another.
- I added cross-links between pages (About → Programmes, Programmes → Contact, Enquiry → Contact and Programmes) and an "Opening hours and maps" link in every footer.
- Email addresses and phone numbers are now clickable `mailto:` and `tel:` links.

### 6.6 Mobile layout
I kept the viewport tag on every page and tested each page at 375px wide; none of them scroll sideways. I also:
- Fixed the mobile menu, which did not open before because `js/script.js` was empty.
- Reduced card padding and made the hero buttons full-width on small screens.
- Added `overflow-wrap` to the location cards so long email addresses can't push the layout wider than the screen.

### 6.7 robots.txt and sitemap.xml
I created both files beside `index.html`:
- `robots.txt` allows all crawlers and points to the sitemap.
- `sitemap.xml` lists the five public pages with a `lastmod` date. I did not include the 404 page, and that page has `<meta name="robots" content="noindex">`.

> **To do after publishing:** both files currently use the placeholder address `https://YOUR-GITHUB-USERNAME.github.io/BrightPath/`. I need to replace it with the real GitHub Pages URL once the site is live.

### 6.8 Speed
- The original photos were 3–5 MB each and up to 4480 × 6720 pixels. I resized and cropped them and converted them to WebP, so they are now **9–74 KB**. That is roughly a 99% reduction, and the total image weight fell from about 12 MB to about 116 KB.
- The team photos use `loading="lazy"` and `decoding="async"`, and they have `width`/`height` attributes so the page doesn't jump while they load.
- The hero image is at the top of the page, so I did **not** lazy-load it. Instead it is preloaded with `<link rel="preload" fetchpriority="high">` so it appears as quickly as possible.
- The script is loaded with `defer`, so it doesn't block the page from rendering.
- The full-size originals are kept locally in `_originals/`, which is listed in `.gitignore` so they won't be uploaded.

### 6.9 Security and privacy
- No passwords, API keys or real personal data are in the code. All contact details are fictional.
- The external Stats SA source link opens in a new tab with `rel="noopener noreferrer"`.
- Both forms clearly state that they are front-end demonstrations that do not send or store data, as the guide says client-side validation is not real form handling. A real version would need a trusted form service or server-side code.
- GitHub Pages serves the site over HTTPS.

### 6.10 Off-page SEO
Off-page SEO happens outside the website, so I wrote it up as a plan in [`docs/OFF_PAGE_SEO_PLAN.md`](docs/OFF_PAGE_SEO_PLAN.md). It contains the guide's student activity:
- three plausible local organisations that might link to the site;
- a polite outreach message;
- one social media post that links to a relevant page.

Because BrightPath is fictional, I did not create a Google Business Profile, add fake reviews or add structured data claiming to be a real organisation. The guide specifically warns against this.

### 6.11 Other improvements I made
- **Fixed hero contrast:** the hero headline was dark text on a dark overlay. It is now white and easy to read.
- **Accessibility:** I added a "Skip to main content" link, a clear yellow focus outline for keyboard users, `aria-current="page"` on the active nav link, titles on the map iframes and `<address>` elements for the addresses.
- **Cleaned up CSS:** I removed unused rules (`.hero:after`, the empty `.hero-overlay` div) and moved inline iframe styles into the stylesheet.
- **404 page:** if someone follows a broken link, they get a branded page with links back to Home and Programmes.
- **Reduced motion:** smooth scrolling and the number animation turn off for users who have reduced motion enabled.

---

## 7. JavaScript functionality (`js/script.js`)

The script file was empty in Part 1, so I wrote it from scratch. It is split into small, commented functions:

1. **Mobile navigation:** the "Menu" button opens and closes the navigation on small screens. It updates `aria-expanded`, changes its label to "Close", and closes when a link is chosen, when Escape is pressed or when the user clicks outside the menu.
2. **Form validation (Enquiry and Contact forms):** any form with `data-validate` is checked when the visitor leaves each field and again on submit. The checks cover required fields, email format, minimum length and the confirmation checkbox. Error messages appear under the field they belong to and are linked with `aria-describedby` for screen readers, and focus moves to the first problem. If everything is valid, the visitor gets a personal thank-you message and the form resets.
3. **Character counter:** message boxes show "X characters remaining" (maximum 1000) and turn red near the limit.
4. **Enquiry pre-fill:** links like `enquiry.html?type=programme&programme=Career%20Ready` automatically select the enquiry type and start the message ("I would like to find out more about joining the Career Ready programme."). The "Enquire about volunteering/sponsoring" buttons use the same feature, so visitors arrive at a form that is already partly filled in.
5. **Live "Open now / Closed" badges (Contact page):** each location shows whether it is open right now and when it next opens, e.g. "Closed now · opens Monday at 08:30". The opening hours are stored in `data-` attributes, and the time is always calculated in South African time (`Africa/Johannesburg`), so the badge is correct wherever the visitor is. It refreshes every minute.
6. **Animated statistic (Home page):** the 45.8% youth-unemployment figure counts up from 0 when it scrolls into view, using `IntersectionObserver`. The real number is already in the HTML, so search engines and visitors without JavaScript still see it.
7. **Footer year:** the copyright year updates automatically.

### How I tested it
- I served the site locally and used headless Chrome to check that the pre-fill selects the right option and fills the message, that empty or invalid fields show the correct errors, that a valid submission shows the thank-you message, and that the menu button opens the navigation.
- I measured every page at 375px wide to confirm there is no sideways scrolling.
- I checked that every page has exactly one `<h1>`, every image has alt text, every external `_blank` link has `noopener`, and every local link points to a file that exists.

---

## 8. Proposed Timeline and Milestones
| Milestone | Planned work |
|---|---|
| Week 1 | Organisation selection, proposal and lecturer approval |
| Week 2 | Research and content sourcing |
| Week 3 | Sitemap, wireframes and visual planning |
| Week 4 | HTML pages and navigation |
| Week 5 | Initial CSS styling and responsive layout |
| Week 6 | Testing, documentation and GitHub submission |
| Week 7 | Part 2: SEO, performance, JavaScript features and publishing |

## 9. Sitemap
Home
- About Us
- Programmes
- Enquiry
- Contact

(The machine-readable version for search engines is `sitemap.xml`.)

## 10. Folder Structure
```text
BrightPath_Part2/
├── index.html
├── about.html
├── services.html
├── enquiry.html
├── contact.html
├── 404.html
├── robots.txt
├── sitemap.xml
├── README.md
├── .gitignore
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
│   ├── favicon.svg
│   ├── youth-group-digital-skills-workshop.webp
│   ├── lebo-mokoena-programme-coordinator.webp
│   ├── karabo-ndlovu-digital-skills-facilitator.webp
│   └── thato-maseko-volunteer-mentorship-lead.webp
├── _originals/            (full-size photos, local only – git-ignored)
├── research/
│   ├── RESEARCH_NOTES.md
│   └── REFERENCES.md
├── wireframes/
└── docs/
    ├── PART1_SUBMISSION_CHECKLIST.md
    └── OFF_PAGE_SEO_PLAN.md
```

## 11. Part 2 Submission Checklist (from the guide)
- [x] Every page has a unique, accurate title and description.
- [x] Pages have a clear main heading and organised section headings.
- [x] Images have useful alt text and sensible file sizes.
- [x] Links explain their destinations; related pages link to one another.
- [x] The mobile layout fits without sideways scrolling.
- [ ] `robots.txt` is beside `index.html` and has the **real** sitemap address *(replace the placeholder after publishing)*.
- [ ] `sitemap.xml` lists the **correct deployed** URLs *(replace the placeholder after publishing)*.
- [x] No passwords, keys, private information or customer data are published.
- [ ] The live site works and its pages, images, links and interactions were checked *(after publishing)*.
- [ ] README includes the repository URL and live URL *(add in section 2)*.

## 12. Changelog
### v0.2 – Part 2: SEO, performance and JavaScript
- Rewrote every page title and meta description around a page-specific search phrase; added Open Graph tags, theme colour and favicon.
- Fixed the heading hierarchy (About page section heading, footer headings, ordered step list).
- Replaced vague "View programme" links with descriptive links to programme anchors; added cross-links and per-programme enquiry links.
- Renamed, resized, cropped and converted all images to WebP (about 12 MB → 116 KB); added descriptive alt text, lazy loading and dimensions; preloaded the hero image.
- Added `robots.txt`, `sitemap.xml` and a `noindex` 404 page.
- Added `rel="noopener noreferrer"` to the external link and privacy notes to both forms.
- Wrote `js/script.js`: mobile menu, accessible form validation, character counter, enquiry pre-fill, live opening-hours badges, animated statistic and automatic footer year.
- Fixed low hero contrast; added a skip link, focus styles, reduced-motion support and better mobile spacing; removed unused CSS.
- Added `docs/OFF_PAGE_SEO_PLAN.md` and SEO references.

### v0.1 – Part 1 Initial Structure
- Created the five required HTML pages.
- Added consistent navigation and footer sections.
- Added fictional organisation content.
- Added programme, enquiry and contact content.
- Added two fictional organisation locations.
- Added responsive CSS foundation.
- Added research notes and references.
- Added wireframe documentation.

## 13. References
See `research/REFERENCES.md` for the full Harvard-style reference list, including the Google Search Central, Sitemaps.org and GitHub Pages guidance I followed in Part 2.

## 14. Important Academic Note
BrightPath Youth Development Foundation, its personnel, addresses, contact details, domain and programme details are fictional. External sources are used only to support research into the social context and rationale behind the proposed organisation.
