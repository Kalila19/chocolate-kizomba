# Chocolate Kizomba

Chocolate Kizomba is a weekly Kizomba class and social night every Tuesday at Be At One, Regent Street, in Soho, London. This website introduces the night to new dancers, explains the classes and prices, and gives people an easy way to book, sign up for a free class or get in touch.

**Live site:** [kalila19.github.io/chocolate-kizomba](https://kalila19.github.io/chocolate-kizomba/)

---

## Contents

- [User experience](#user-experience)
- [Features](#features)
- [Future features](#future-features)
- [Design](#design)
- [Accessibility](#accessibility)
- [Technologies](#technologies)
- [Testing](#testing)
- [Bugs fixed](#bugs-fixed)
- [Deployment](#deployment)
- [Credits](#credits)

---

## User experience

### Target audience

- People in London curious about trying Kizomba for the first time
- Dancers with some experience looking for a regular class and social
- Existing community members checking times, prices and upcoming news

### User goals

- Understand what Chocolate Kizomba is and what a Tuesday night involves
- Find class times, levels and prices quickly
- Book a class or sign up for a free first class
- Find out how to get there
- Ask a question and get a reply

### Site owner goals

- Bring new dancers to the Tuesday classes
- Grow the mailing list
- Reflect the friendly, welcoming feel of the community

---

## Features

### On every page

- **Navbar:** fixed to the top of the screen, with the logo linking home. The current page is highlighted. On small screens it collapses into a menu button.
- **Footer:** contact email (clickable), venue address, links to Instagram, Facebook, TikTok and the WhatsApp group, quick links to key sections, and a mailing list sign-up (shown from 992px wide).
- **Page fade:** each page fades in on load (skipped for visitors with reduced motion turned on).

### Home (`index.html`)

- Hero image with the headline "London's most soulful Kizomba night" and a **Book now!** button
- Photo carousel next to a sign-up form for a free class
- "Why dance with us?" cards: levels for everyone, community, music and confidence

### Classes (`classes.html`)

- Schedule, prices and levels for the class and social, alongside the event flyer
- **Book a class** button linking to the booking page
- Meet your instructors cards
- FAQs using expandable `<details>` sections

### Contact Us (`contact-us.html`)

- Contact form (name, email, subject, message) sent with Web3Forms, with hidden spam protection
- Connect with us links (WhatsApp, Instagram, Facebook)
- Opening hours, venue address and a **Get Directions** link to Google Maps

### Message sent (`success.html`)

- Thank-you page shown after the contact form is submitted, with a link back to the home page
- Hidden from search engines with `noindex`

### Signed up (`thank-you.html`)

- Thank-you page shown after someone joins the mailing list, from either the free-class sign-up on the home page or the footer sign-up on any page
- Confirms the free class is on its way, with a link back to the home page
- Hidden from search engines with `noindex`

---

## Future features

- **About us page:** the story behind Chocolate Kizomba and the team
- **Workshops page:** upcoming workshops with booking links (under "Learn to dance")
- **Events page:** calendar of socials and special events
- **Gallery page:** photos and videos from past nights
- **Mailing list:** move the free-class and footer sign-up forms from Web3Forms to Mailjet, so subscribers go straight onto a mailing list instead of arriving as emails
- **Instructor bios and photos** on the Classes page
- **Privacy policy page**, linked from the sign-up forms

The About us, Workshops, Events and Gallery links already appear in the navbar as placeholders (`href="#"`) to show the planned site structure.

---

## Design

### Colour palette

| Colour | Hex | Used for |
|---|---|---|
| Dark Amethyst | `#45134f` | Navbar, footer, hero overlay |
| Cocoa Brown | `#5b3a32` | Main body text |
| Royal Orchid | `#8125a0` | Links and button hover |
| Pumpkin Spice | `#f47b35` | Call-to-action buttons |
| Sunlit Clay | `#deb46d` | Current page in the navbar |
| Ivory/Linen | `#f6f0e8` | Page background, footer text |
| Charcoal | `#17131a` | Button text |

All text and background combinations were chosen to meet WCAG AA contrast. For example, Charcoal text on the orange buttons has a contrast ratio of about 6.8:1.

### Typography

- **Montserrat** for headings, card titles and FAQ questions
- **Poppins** for body text

Both are loaded from Google Fonts.

### Imagery

Photos are from Chocolate Kizomba nights at Be At One. They were resized (maximum 1920px wide) and compressed so pages load quickly.

### Layout

The site is built mobile-first with Bootstrap's grid, with layout changes at 768px, 992px and 1200px. For example, the "Why dance with us?" cards show one per row on phones, two on tablets and four on desktops.

---

## Accessibility

- Logical heading order on every page (`h1`, then `h2`, then `h3`), using Bootstrap's heading classes to control size separately
- Descriptive `alt` text for every image
- Labels for every form field, with `autocomplete` to help people fill them in
- `aria-label`s on icon-only links (the footer social icons), and decorative icons hidden from screen readers
- Visible focus states on buttons and links
- `lang="en-GB"` on every page
- Fade animation turned off for visitors with reduced motion turned on

---

## Technologies

- HTML5 and CSS3
- [Bootstrap 5.3](https://getbootstrap.com/): grid, navbar, carousel, cards and forms
- [Font Awesome](https://fontawesome.com/): icons
- [Google Fonts](https://fonts.google.com/): Montserrat and Poppins
- [Web3Forms](https://web3forms.com/): sends contact form messages and mailing list sign-ups to email
- [favicon.io](https://favicon.io/): favicons
- Git, GitHub and GitHub Pages: version control and hosting
- Visual Studio Code

---

## Testing

> Rows left blank are still to be tested.

### Validators

| Page | W3C HTML validator | Result |
|---|---|---|
| index.html | 0 errors, 0 warnings | Pass |
| classes.html | 0 errors, 0 warnings | Pass |
| contact-us.html | 0 errors, 0 warnings (after removing `autocomplete` from the hidden spam-check checkbox, which isn't allowed on checkboxes) | Pass |
| success.html | 0 errors, 0 warnings | Pass |
| thank-you.html | | |

| File | W3C CSS validator | Result |
|---|---|---|
| styles.css | 0 errors. 3 standard notices: the Google Fonts `@import` isn't checked, and CSS variables aren't checked | Pass |

### Lighthouse

| Page | Performance | Accessibility | Best Practices | SEO |
|---|---|---|---|---|
| index.html | | | | |
| classes.html | | | | |
| contact-us.html | | | | |

### Responsiveness

Checked with screenshots in Microsoft Edge. Still to check by hand in DevTools: 375, 576, 992 and 1400px.

| Page | 320px | 768px | 1200px | Notes |
|---|---|---|---|---|
| index.html | Pass | Pass | Pass | Cards: 1, then 2, then 4 per row. Carousel and sign-up stack on mobile, side by side from 768px |
| classes.html | Pass | Pass | Not yet | Hero grows to fit its text on mobile. Details switch to label/value pairs from 576px |
| contact-us.html | Pass | Not yet | Pass | Form, then Connect / Opening Hours / Find us in three columns from 768px |
| success.html | Pass | Pass | Not yet | Message shows above the photo on mobile, beside it from 768px |
| thank-you.html | | | | Same layout as success.html |

No page scrolls sideways at 320px.

### Manual testing

| Test | Expected result | Result |
|---|---|---|
| Navbar links | Each link opens the right page | Pass (every local link and image checked with a script; About us, Workshops, Events and Gallery are planned placeholders) |
| Mobile menu | Opens, dropdown works, closes | |
| Footer quick links | Open the right section of the Classes page | Pass (`#faqs`, `#instructors` and `#classes` all exist) |
| Social links | Open in a new tab | WhatsApp, Instagram, TikTok, Google Maps and Afromoya all respond. Facebook blocks automated checks, so test it by hand |
| Contact form, empty submit | Browser asks for the missing fields | |
| Contact form, invalid email | Browser asks for a valid email | |
| Contact form, real message | Email arrives and success.html is shown | |
| Free-class sign-up (home page), real email | Email arrives and thank-you.html is shown | |
| Footer sign-up (each page, from 992px), real email | Email arrives and thank-you.html is shown | |
| Sign-up forms, empty or invalid email | Browser asks for a valid email | |
| Book now / Book a class | Booking page opens in a new tab | |
| Keyboard only | Every link and button can be reached and focus is visible | |

### Browsers

Chrome, Firefox, Safari (including iOS) and Edge.

---

## Bugs fixed

| Bug | Fix |
|---|---|
| Thin gap between the fixed navbar and the hero after changing the font | Updated the body's `padding-top` to match the navbar's new height |
| Headings linked from the footer were hidden under the fixed navbar | Added `scroll-padding-top` to `html` |
| White text on orange buttons failed contrast checks (2.7:1) | Changed button text to Charcoal (6.8:1) |
| Buttons grew on hover and went see-through when clicked | Styled buttons through Bootstrap's `--bs-btn-*` variables |
| Hero text was cut off on small phones | Changed the hero from `height` to `min-height` |
| The `h3+.h5` selector didn't style headings | Changed it to `h3, .h5` |
| Images used backslashes in their paths, which break on web servers | Changed every path to forward slashes |
| Large images (up to 6MB each) slowed the pages | Resized and compressed every image (106MB down to about 8MB) |

---

## Deployment

The site is hosted on GitHub Pages.

1. In the GitHub repository, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose the **main** branch and the **/ (root)** folder, then click **Save**.
4. After a minute or two the site is live at `https://kalila19.github.io/chocolate-kizomba/`.

### Running it locally

1. Clone the repository: `git clone https://github.com/Kalila19/chocolate-kizomba.git`
2. Open `index.html` in a browser.

The site uses web-ready copies of the photos in `assets/images/resized/`.

---

## Credits

- Layout components: [Bootstrap](https://getbootstrap.com/)
- Icons: [Font Awesome](https://fontawesome.com/)
- Fonts: [Google Fonts](https://fonts.google.com/)
- Favicons: [favicon.io](https://favicon.io/)
- Contact form handling: [Web3Forms](https://web3forms.com/)
- Bookings: [Afromoya](https://www.afromoya.com/)
- Photos: Chocolate Kizomba
