# Liberty Autogas Conversions: redesign mockup

> **Pitch points below were written when the site was built and most haven't been rechecked.** The call script in `sales/sales-scripts.md` was corrected on 24 Nov 2026 and is safer than this list. Check each one on the live site, on a real phone, before saying it.

Rebuild of http://libertyautogas.com.au (the autogas/LPG site only, not the Liberty Mechanics mechanical side).
Plain HTML/CSS/JS, no build step. Open `index.html` in a browser, or serve the folder with any static server.

## Pages

| File | Old page | What's on it |
|---|---|---|
| `index.html` | `index.php` | Hero, the four services (LPG conversions, tank testing, dyno testing, gas servicing), the three "why convert" panels, diesel conversions / The Gas Guru |
| `about.html` | `about_us.php` | Family business since 2006, Dennis Kenworthy "The Gas Guru", diesel and petrol conversions, onsite testing |
| `conversions.html` | `conversions.php` | How autogas works, install diagram, changeover switch and Lambda unit, safety, kit brands |
| `lpg-tank-testing.html` | `lpg-tank-testing.php` | 10-year testing rule, licensed in-house testing |
| `faq.html` | `faq.php` | All 9 FAQs as tap-to-open accordions |
| `environment.html` | `environment.php` | Emissions text, plus the petrol/diesel comparison as bar charts |
| `benefits.html` | `benefits.php` | Advantages over other fuels, "Facts about fuels" table |
| `savings.html` | `savings.php` | Savings text and figures (linked from the old site but not in its menu) |
| `contact.html` | *(none: old "Contact Us" was just an email link)* | Phone, email, address, Google map |

Shared: `css/style.css`, `js/main.js` (mobile menu and footer year only).

## What changed vs the old site (sales pitch points)

- **Works on phones.** The old site has a fixed 1000px layout and a 1024px minimum-width background, so on a phone the header, menu and phone number get cut off or shrink to unreadable. The new one is fully responsive: hamburger menu, readable text at 375px, no sideways scrolling. Checked at 375px, 768px and 1280px.
- **Tap-to-call everywhere.** On the old site the phone number and address are baked into the logo image, so customers can't tap or copy them. The new site has a call button in the header, a sticky "Call now / Find us" bar on phones, and call buttons on every page.
- **A real Contact page.** The old "Contact Us" only opened an email. Now there's a page with phone, email, address, a map and a Google Maps directions link.
- **Up-to-date footer.** The old footer says © 2012. The new one shows the current year automatically and keeps the licence number (MRB495) and MTA WA membership.
- **Same brand, modernised.** It keeps their cyan (#0CF), the blue-flame background and the torch logo, and adds the orange from the torch flame and the "Now converting hybrid cars!" badge as the button colour.
- **Easier to read.** Long text blocks are now split into headings, tick lists, stat tiles, an FAQ accordion and bar charts. Every page has a sidebar with a call button and the Savings / Environment / Benefits links.
- **Polish pass:** dark mode (follows the phone/computer setting, with a sun/moon toggle in the header that remembers the choice and no flash on load), fade-up reveals on scroll, smooth hovers, a smooth mobile menu and FAQ open/close, a sticky header that blurs once you scroll, back-to-top button, count-up numbers on Savings, lazy-loaded images and visible keyboard focus. All motion switches off for people who turn on "reduce motion".
- **Better for Google.** Each page has its own title and description, and the old site's tracking code (Universal Analytics `_gaq`, which Google shut down) has been removed.

## Content notes (check with the owners)

- Text is theirs, lightly tidied: spelling fixes (for example "reqular" → "regular", "abundent" → "abundant") and a few small grammar fixes.
- **One maths fix:** the old FAQ says LPG saves "$72.00" on a $120 fill when LPG costs $64. The real saving is $56, so the new page says $56.
- Removed "with the continuation of the government's rebates", because the LPG rebate scheme ended years ago.
- Removed "the country's entire taxi fleet" from the engine-damage FAQ because it's out of date.
- The conversion price guide in the FAQ ($2,200–$4,000) and the $1.50/L example are **their own figures from about 2012**. They're kept because they're on the live site, but the owners should confirm or update them before go-live.
- Experience dates on the old site don't agree with each other: "since 1984" (home), "since 1985" (Dennis, about page) and "over 40 years" (tank testing). Each is kept where it originally appeared. Worth confirming.
- **No opening hours** are on the old site, so none are shown. Add them if the owners provide them.
- The old home banner was a stock photo with a quote ("I save so much more money on LPG…"). It's left out because it isn't a real customer testimonial.

## Images (all from libertyautogas.com.au/images/)

| File | Source | Used for |
|---|---|---|
| `liberty-autogas-logo.png` | Cropped from `LAG_New_Logo2.png` (left 500px). The phone and address text were removed so the logo scales on mobile and the details can be real, tappable text | Header and footer logo |
| `PageBG1.jpg` | `PageBG1.jpg` | Blue-flame hero and page-header background |
| `gas-convertions-rockingham-hybrid-cars.png` | Same name | "Now converting hybrid cars!" badge on the home hero |
| `installthumb.gif` | Same name | LPG installation diagram (home, conversions) |
| `autoswitch.gif` | Same name | Changeover switch (conversions) |
| `controler.gif` | Same name | Lambda control unit (conversions) |
| `MTA_Logo.png` | Same name | MTA WA member badge (footer) |

Icons are inline SVGs. Fonts are Inter and Barlow from Google Fonts. The contact page map is a Google Maps embed of 3/7 McCamey Road.
