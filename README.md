# CGPA to Percentage Calculator — AdSense-Ready Setup Guide

Your site is now structured the way AdSense reviewers expect. Below is exactly what you need to do before submitting your application.

---

## Files in this package

| File | Purpose | Required? |
|---|---|---|
| `cgpa-to-percentage.html` | Your main landing page (updated footer) | ✅ Yes |
| `about.html` | About Us page | ✅ Yes |
| `contact.html` | Contact page with email form | ✅ Yes |
| `privacy-policy.html` | Privacy Policy (AdSense-compliant) | ✅ **CRITICAL** |
| `terms.html` | Terms of Service | ✅ Yes |
| `disclaimer.html` | Disclaimer with ad-disclosure | ✅ Yes |
| `robots.txt` | Search engine instructions | ✅ Recommended |
| `sitemap.xml` | Page index for Google | ✅ Recommended |
| `ads.txt` | AdSense fraud-prevention file | ✅ After approval |

---

## Step 1 — Replace ALL placeholders before going live

Search every HTML file (Find &amp; Replace across files in VS Code, Sublime, or your editor) for these strings and replace them with your real values:

| Find | Replace with |
|---|---|
| `example.com` | Your real domain (e.g. `cgpacalc.in`) |
| `https://example.com` | Your real full URL (e.g. `https://cgpacalc.in`) |
| `hello@example.com` | Your real general contact email |
| `support@example.com` | Your bug/support email (can be same as above) |
| `partners@example.com` | Your business email (can be same as above) |
| `CGPA to Percentage Calculator` | Your real brand name *(optional — only if different)* |

**Also check:** the `<link rel="canonical">` tag at the top of every page — these all currently point to `example.com`.

### File-by-file canonical URLs to update:
- `cgpa-to-percentage.html` line 14
- `about.html`, line ~14
- `contact.html`, line ~14
- `privacy-policy.html`, line ~14
- `terms.html`, line ~14
- `disclaimer.html`, line ~14

---

## Step 2 — Decide your homepage URL strategy

Option A (recommended): **Rename `cgpa-to-percentage.html` to `index.html`** so your homepage is `https://yourdomain.com/` instead of `https://yourdomain.com/cgpa-to-percentage.html`.

If you do this, also update the footer/nav links across all 5 other pages — search for `cgpa-to-percentage.html` and replace with `index.html`.

Option B: Keep it as is, and configure your web host to redirect `/` to `/cgpa-to-percentage.html`.

---

## Step 3 — Add your Google Analytics &amp; Search Console

Before applying to AdSense, you should:

1. **Verify your domain in [Google Search Console](https://search.google.com/search-console)** — submit your `sitemap.xml` once verified.
2. **Add Google Analytics (GA4)** — paste the snippet into the `<head>` of each HTML file just before `</head>`.
3. **Let it accumulate ~2–4 weeks of organic traffic** before applying. Sites with zero traffic are commonly rejected.

---

## Step 4 — Apply for Google AdSense

1. Go to [adsense.google.com](https://adsense.google.com) and sign up.
2. Enter your verified domain.
3. Add the AdSense verification code to the `<head>` of all your pages (Google will give you a unique snippet — looks like `<script async src="...adsbygoogle.js?client=ca-pub-..."></script>`).
4. Submit your site for review.
5. Wait — review takes anywhere from 1 day to 4 weeks.

---

## Step 5 — After you're approved

1. Open `ads.txt` in this folder.
2. Replace `pub-XXXXXXXXXXXXXXXX` with your actual publisher ID (you'll find it in your AdSense dashboard — it looks like `pub-1234567890123456`).
3. Upload `ads.txt` to the **root** of your domain so it's accessible at `https://yourdomain.com/ads.txt`.
4. Place ad units in your pages where appropriate (NOT in the policy pages — AdSense allows ads on those, but cleaner brand-image keeps them ad-free).

---

## Common AdSense rejection reasons — and how this package addresses them

| Rejection reason | Status in your site |
|---|---|
| "Insufficient content" | ✅ Your main page has substantial original content: FAQs, formulas, tables, university breakdown |
| "Missing privacy policy" | ✅ Comprehensive privacy policy with AdSense, cookies, and DART cookie disclosures |
| "Missing/unclear navigation" | ✅ Footer of every page links to About, Contact, Privacy, Terms, Disclaimer |
| "No way to contact the publisher" | ✅ Contact page with email and form |
| "Site under construction" | ⚠️ Make sure every link works and no "Coming soon" / "TBD" exists |
| "Domain mismatch" | ⚠️ Apply to AdSense with the exact same domain your site is on |
| "Site doesn't comply with policies" | ⚠️ Don't run any other competing ad networks during application |
| "Low traffic / brand-new domain" | ⚠️ Wait 2–4 weeks after launch before applying |

---

## Things to add that will strengthen your application

Optional but recommended:

1. **A blog or articles section** — Even 3–5 well-written articles (e.g., "How to calculate SGPA", "What is a good CGPA for an MS abroad", "VTU grading system explained") significantly boost approval odds. AdSense loves content depth.
2. **Internal linking** — Within your main page content, link to your About and Contact pages naturally (e.g., "Read about our methodology" → about.html).
3. **An author byline** — On articles, add a real (or pseudonymous) author with a one-line bio. Shows real human authorship.
4. **Social profiles in footer** — Even Twitter and LinkedIn icons help signal legitimacy. Add them next to the Legal column if you have any.

---

## Things to AVOID until approval

- ❌ Don't put placeholder text like "Lorem ipsum" anywhere
- ❌ Don't link to any non-existent pages (every link must work)
- ❌ Don't use copyrighted images (your site is text/SVG-only — perfect)
- ❌ Don't run pop-ups, intrusive ads, or auto-playing media
- ❌ Don't use other ad networks (e.g., Media.net, PropellerAds) simultaneously
- ❌ Don't have a "thin content" site with fewer than ~30 lines of unique text per page (your main page already passes; the policy pages have substantial text too)

---

## Quick local preview

To test the site locally before deploying:

```bash
# In the folder containing all these files
python3 -m http.server 8080
# Then open http://localhost:8080/cgpa-to-percentage.html
```

Click through every footer link to confirm all pages load and nav works.

---

## After AdSense approval — placing ad units

When you get approved and want to place ads, the natural slots in your main page are:

1. **Between Hero and "What is CGPA"** section — a horizontal display ad
2. **Between "Formula" and "How to use"** — a responsive in-article ad
3. **Between "Conversion Table" and "FAQ"** — a multiplex/native ad
4. **In the sidebar of policy pages** — optional, single ad

Avoid placing ads:
- Inside the calculator card itself
- Above the fold on the hero (hurts user experience)
- Stacked back-to-back (violates AdSense layout policy)

---

Good luck with your AdSense application! Your site has a strong foundation — the original calculator content is genuinely useful and well-written, which is the single biggest factor reviewers care about.
