# Sounds Like Soma website — portfolio write-up

Copy for the `/portfolio` page in `web-wizard-dev-v2`, resumes and posts. It describes the
project **as of 2026-10-18, commit `a96904f`** (branch `master`, with uncommitted work in the
tree: this file and the `- docs` line in `_config.yml`). No commits since 2026-09-24, so this
run re-checked the numbers only. Every number in it has a row in [Evidence](#evidence) with
the command or file to re-check it. Run `/portfolio-writeup numbers` to refresh them.

The site is live at `www.soundslikesoma.com` (Jekyll on Netlify) and has been maintained since
May 2020. Most of the work happened in 2020–2023; since then it has had occasional updates,
the latest a Ruby and Jekyll upgrade in February 2026.

## Before publishing

None of these blocks the site entry, which has been published since 2026-10-05 (no `draft`).
They are for committing this file and for the owner's records.

1. **Keep this file off the live site.** This is a Jekyll site, and Jekyll publishes every
   file that is not excluded. `- docs` was added to `exclude:` in `_config.yml` on
   2026-09-24, with this file. A local build then left `docs/` out; without the line, the
   same build published `docs/portfolio-writeup.md`. Commit both together, and after the
   next deploy check that `/docs/portfolio-writeup.md` returns 404. Re-checked 2026-10-18:
   both are still uncommitted, the live URL is 404 (nothing deployed yet), and `/CNAME` is
   200, so every other unlisted file is still published.
2. **The relationship is framed as client work** (the owner's choice, per
   `web-wizard-dev-v2/docs/portfolio.md`). A reader who clicks through will see more than an
   arm's-length client: the live site names Zack as the studio's engineer ("Call Zack",
   "Studio A with Engineer Zack Hanni") and links his LinkedIn, and its "Artist Website
   Design" service page (since 2024-05-16) sends artists to "our partners at Web Wizard
   Development". That service card is also visible at the bottom of the portfolio cover.
   Nothing in the copy below claims more distance than that, and the resume bullets say
   "built and maintained" (checklist R3). Confirm the framing still suits you.
3. **The cover stays as it is** (2026-10-18: the owner took the default). It is a live capture
   of the home page (`soma/home-page.jpg`, 2026-09-26) and reproduces the studio's public
   contact box (two first names with phone numbers, one of them the owner's, and the studio
   email) and its hero photo of a person at the mixing desk. It has been on the portfolio since
   2026-09-26. If the studio ever objects, crop the shot below the contact box or retake it.
4. **An unfinished rebuild is public.** `sounds-like-soma.vercel.app` (the Next.js rebuild,
   last deployed 2025-04-19) returns 200 with a 404 page body and a footer linking to
   unrelated sites (the 200 and the 404 body re-checked 2026-10-18). It is not on the studio's domain and is not
   mentioned below. Decide whether to take it down.

The two results the original entry claimed without a source ("consistently ranks on Page 1",
"measurable boost in booking inquiries") stay out of the copy; Numbers still to get has the
questions that would bring them back.

---

## One-line pitch

A fast static website for a Philadelphia recording studio, with a page for every service it
sells and online booking through Square, built and kept current since 2020.

## The problem

Sounds Like Soma is a recording, mixing and mastering studio in South Philadelphia. It sells
many separate services (studio time in several rooms, mixing and mastering, podcast and
voice-over recording, room rental), and each competes for its own local searches such as
"recording studio Philadelphia". Work on the site started in 2020 from a free Jekyll theme.

What the studio needed:

- A page for each service that people searching locally can find, with prices and answers to
  common questions.
- Proof of the work: real releases recorded there, and real reviews.
- A way for artists to book and pay without calling first.
- A site that stays fast on phones, costs little to run, and keeps working for years.

## What it does

- **10 service pages** (7 listed, 3 held back from the listing), each with its own title,
  meta description and wording aimed at Philadelphia searches. 7 of them end with an FAQ
  section.
- **Work samples:** 12 releases recorded at the studio, each with an embedded YouTube or
  Spotify player.
- **Reviews:** 8 endorsements taken from the studio's Google Maps reviews.
- **A blog** of 4 posts on recording, mixing and podcasting.
- **Online booking and payment:** 8 Square booking and checkout links, one for each room or
  service.
- **Structured data:** the home page carries LocalBusiness data and 6 service offers with
  prices, so search engines can show the studio's details.
- **Built for speed and safety:** WebP images, below-the-fold images and embeds loaded lazily,
  and security headers (Content-Security-Policy, X-Frame-Options, X-Content-Type-Options and
  HSTS) on Netlify.

## Ready-to-paste portfolio entry

Matches the `Project` interface in `web-wizard-dev-v2/lib/portfolio-data.ts` (working tree
on `main`, `bf2e9316`, checked 2026-10-18). It **replaces** the live entry and keeps its slug,
`seo-static-generation`. It starts from that live entry, not from this file's 2026-09-24 block:
the site has since added `features` (with icons), `sectors`, `location`, `featured`, the new
cover and a shorter `description`, and the old block no longer compiles (it lacks the
required `sectors`). Every image path exists in `public/portfolio_images/`.

```ts
  // Sounds Like Soma
  {
    slug: "seo-static-generation",
    title: "Recording Studio Website & Local SEO",
    description:
      "A fast static site for a Philadelphia recording studio: a page for each service, work samples, Google reviews and online booking, kept current since 2020.",
    outcome:
      "Gave a Philadelphia recording studio a page for every service it sells, where artists can hear its work and book and pay online, on a static site kept current since 2020.",
    industry: "Music & recording studio",
    client: "Sounds Like Soma",
    overview:
      "Sounds Like Soma is a recording, mixing and mastering studio in South Philadelphia. Starting in 2020 from a free Jekyll theme, the site grew into 10 service pages written for Philadelphia searches, 7 of them with FAQ sections, plus 12 work samples with embedded players, 8 reviews from the studio's Google Maps listing and a blog. Artists can book and pay online through Square. A 2022 SEO overhaul added meta descriptions, a sitemap and LocalBusiness structured data; in 2023 the site moved from GitHub Pages to Netlify with security headers; and in 2026 it was upgraded from an end-of-life Ruby to Ruby 3.3.6.",
    features: [
      {
        title: "A page for every service",
        icon: "file",
        description:
          "10 service pages, each with its own title, meta description and wording aimed at Philadelphia searches. 7 of them end with an FAQ section.",
      },
      {
        title: "Work samples",
        icon: "music",
        description: "12 releases recorded at the studio, each with an embedded YouTube or Spotify player.",
      },
      {
        title: "Reviews",
        icon: "star",
        description: "8 endorsements taken from the studio's Google Maps reviews.",
      },
      {
        title: "A blog",
        icon: "newspaper",
        description: "4 posts on recording, mixing and podcasting.",
      },
      {
        title: "Online booking and payment",
        icon: "calendar",
        description: "8 Square booking and checkout links, one for each room or service.",
      },
      {
        title: "Structured data",
        icon: "code",
        description:
          "The home page carries LocalBusiness data and 6 service offers with prices, so search engines can show the studio's details.",
      },
      {
        title: "Built for speed and safety",
        icon: "zap",
        description:
          "WebP images, below-the-fold images and embeds loaded lazily, and security headers (Content-Security-Policy, X-Frame-Options, X-Content-Type-Options and HSTS) on Netlify.",
      },
    ],
    categories: [
      PortfolioCategory.Website,
      PortfolioCategory.Redesign,
      PortfolioCategory.ECommerce,
    ],
    sectors: ["music"],
    location: "Philadelphia",
    // 4: off the home page, but first in line if a project above it goes back to draft
    featured: 4,
    services: ["website-development", "update-existing-website"],
    scope: [
      "Local SEO",
      "Service landing pages",
      "Structured data (JSON-LD)",
      "Online booking & payments",
      "Performance optimization",
      "Hosting migration",
      "Ongoing maintenance",
    ],
    platforms: ["Web"],
    technologies: ["Jekyll", "Ruby", "Sass", "Netlify", "JSON-LD", "Google Analytics 4", "Square"],
    cover: {
      src: "/portfolio_images/soma/home-page.jpg",
      alt: "Sounds Like Soma home page headed Music Recording Studios in Philadelphia, with a studio photo and a Book a Session button",
    },
    gallery: [
      {
        src: "/portfolio_images/soma/recording-service-page.jpg",
        alt: "Recording studio service page headed Mix Music Recording Studios Philly",
        caption: "Each service has its own page, written for the searches clients use",
      },
      {
        src: "/portfolio_images/soma/reviews-page.jpg",
        alt: "Reviews page featuring endorsements pulled from Google Maps",
        caption: "Reviews taken from the studio's Google Maps listing",
      },
      {
        src: "/portfolio_images/soma/samples-page.jpg",
        alt: "Music samples page introducing embedded songs and videos",
        caption: "Work samples with embedded YouTube and Spotify releases",
      },
    ],
    metrics: [
      { value: "6 years", label: "maintaining the studio's site (2020-2026)" },
      { value: "100", label: "Lighthouse accessibility and SEO on the home and recording studio pages (mobile, Oct 2026)" },
    ],
    externalLink: "https://www.soundslikesoma.com",
    year: "2020",
    duration: "2020 to present",
    challenges: [
      "The studio sells many separate services, and each one competes for its own local searches. The starting point was a free Jekyll theme with placeholder content and no page for any of them.",
      "Artists want to hear the studio's work and check prices before they commit, and then book without having to call first.",
      "Search engines had little to go on: pages were missing meta descriptions, there was no structured data describing the business, and several internal links redirected or broke.",
      "The pages are photo-heavy and embed music and video players, which slows a phone down.",
      "The site ran on free GitHub Pages hosting with no control over security headers, and by 2026 its build still used Ruby 2.6.5, which reached end of life in 2022.",
    ],
    solutions: [
      "Built 10 service pages, each with its own title, meta description and Philadelphia-focused wording, 7 of them with an FAQ section, and wrote 4 blog posts around the same topics.",
      "Added a samples page with 12 releases recorded at the studio, a reviews page with 8 endorsements from Google Maps, and 8 Square booking and checkout links so artists can book and pay online.",
      "Ran an SEO overhaul in late 2022: meta titles and descriptions matched to page content, a sitemap without utility pages, fixes from a Seobility audit, and LocalBusiness plus 6 service-offer structured data on the home page.",
      "Converted the image library to WebP and lazy-loaded images and social embeds below the fold, while keeping above-the-fold images eager.",
      "Moved hosting to Netlify in February 2023 and added Content-Security-Policy, X-Frame-Options and X-Content-Type-Options headers. In 2026, upgraded Ruby 2.6.5 to 3.3.6 and Jekyll 4.3.1 to 4.4.1, and fixed the template errors the upgrade exposed.",
    ],
    results: [
      "20 pages in the live sitemap: 10 service pages, 4 blog posts, and pages for samples, reviews, contact and services.",
      "100 Lighthouse scores for accessibility and SEO on the home page and the recording studio page (mobile, Oct 2026).",
      "LocalBusiness and 6 service-offer structured data on the home page, and Content-Security-Policy, X-Frame-Options, X-Content-Type-Options and HSTS headers served on every page.",
      "The build moved off Ruby 2.6.5, end-of-life since 2022, to Ruby 3.3.6 and Jekyll 4.4.1.",
      "413 updates since 2020, 58 of them for SEO, on static hosting with no server to run.",
    ],
  },
```

### Notes on that entry

#### Audit of the current site entry (2026-10-18)

The live `seo-static-generation` entry (web-wizard `main`, `bf2e9316`), claim by claim
(checklist E5). Everything not listed was re-checked and kept as it is.

| Live claim | Verdict | Evidence |
| --- | --- | --- |
| Metric tile "413 updates shipped since 2020, 58 of them for SEO" | moved to `results` (already there) | True (re-counted 2026-10-18), but a commit count is an engineering number. The site's own rule (`docs/portfolio.md` → Writing rules) and checklist E4 keep commit counts out of tiles. 2 tiles remain, which the page shows as a 2-wide grid |
| Tile and result "100 Lighthouse accessibility and SEO on the live home page (mobile, Sep 2026)" | keep, re-measured, widened | 2026-10-18: accessibility 100 and SEO 100 on the home page **and** `/services/recording-studios/`. Not on every page: `/samples/` scores accessibility 91 (embed frames without titles, links told apart by color only) and `/reviews/` 95 (links told apart by color only); SEO is 100 on all 4. The copy names the 2 pages it covers |
| Result "Artists book and pay for studio time, mixing, mastering and podcast sessions online through 8 Square links" | removed from `results`; kept as a feature | The 8 links work (each answered 200 on a fresh first visit, 2026-10-18), but nothing on record shows artists using them, and checklist C1 needs a count of real use before a result says they do. "Online booking and payment" in `features` still describes them. Bring the result back with a bookings figure (Numbers still to get) |
| Overview "Artists book and pay online through Square." | reworded to "can book" | Same reason |
| Cover `soma/home-page.jpg` | keep (owner, 2026-10-18) | A real capture of the live home page (2026-09-26, 1600×1000) that already replaced the mock-up. `web-wizard-dev-v2/docs/portfolio.md`'s per-project row still calls the cover a mock-up: that row is stale. See Before publishing, the cover item |
| "10 service pages", "7 of them with FAQ sections" | keep | Re-counted. The 10 are every page under `/services/`: 9 services plus a studio gear list, which the site lists as a service |
| `featured: 4`, `sectors: ["music"]`, `location: "Philadelphia"` | keep | Set on the site (owner, 2026-10-03 and 2026-10-05) |

#### Audit of the old entry (2026-09-24)

**What changed from the original entry, and why** (checklist E5):

| Old claim | Verdict | Evidence |
| --- | --- | --- |
| "since 2020", "6 years" | keep | First commit by Zack 2020-05-13; the earlier commits are the theme's author |
| "six years of **continuous** SEO / ongoing SEO program" | unsourced, softened | Zack's commits by year: 42, 28, 213, 123, then 4, 1, 2 (2024–2026). SEO-titled commits stop in 2023. Say "maintained", unless SEO work happened outside the repo (ask) |
| "12 embedded work samples" | keep | 12 files in `_samples/`, all with a YouTube or Spotify embed |
| "reviews sourced from Google" | keep | 8 files in `_reviews/`; `reviews.md` says they are from Google Maps |
| "FAQ sections" | keep | 7 of 10 service pages |
| "book and pay through Square" | keep | 8 Square links in `_includes/booking-buttons/` |
| "LocalBusiness and service-offer structured data" | keep | Live home page: 1 LocalBusiness + 6 Product offers |
| "80+ SEO updates" | replaced | 58 commits with SEO terms in the subject (the regex is in Evidence). 80+ could not be reproduced |
| "400+ updates since 2020" | keep, exact | 413 commits by Zack since 2020-05-13 |
| "fixes from Seobility site audits … tracked with Google Analytics 4 and Ahrefs" | keep, not in copy | Commit `294eaaa` (Seobility), GA4 tag `G-…` in `_includes/google-analytics.html`, `ahrefs-site-verification` in `_layouts/default.html` |
| "WebP, lazy-loaded, hero eager" | keep | Commits 2022-10-31 to 2023-02-07 |
| "GitHub Pages to Netlify with security headers" | keep | `move from github to netlify` 2023-02-01; `netlify headers` 2023-02-09; live headers checked |
| "Ruby 3.3 and Jekyll 4.3 in 2026" | corrected | Ruby 2.6.5 → 3.3.6; the Gemfile asks for Jekyll `~> 4.3` and the lock resolved **4.4.1** |
| "Consistently ranks on Page 1 of Google for targeted local keywords" | unsourced, removed | No ranking data in any repo. Needs Search Console (Numbers still to get) |
| "Measurable boost in studio booking inquiries" | unsourced, removed | No booking data. Needs Square or Analytics numbers |
| "100 Lighthouse accessibility and SEO (mobile, Sep 2026)" | unsourced, removed | No recorded run anywhere. Re-measure |
| "Achieving fast page loads … Core Web Vitals" (challenge) | reworded | Speed work is real; no measurement exists, so no CWV claim |
| "Low maintenance and hosting cost" | kept without a number | Static site, no server. Hosting cost is owner-only |

- **`metrics`**: 2 tiles. "6 years" is the client relationship, and "100" is the quality score
  re-measured on 2026-10-18. The "413 updates" tile moved to `results` (audit above). A Search
  Console or bookings figure would make a stronger tile once the owner has one.
- **`externalLink`** uses `www.`, because the apex 301s to it.
- **Framing** (Before publishing, the framing item): if you decide to say the relationship
  plainly, change the overview's first sentence to "...in South Philadelphia, where I also
  work as an engineer."

## Resume bullets

- Built and maintained a Philadelphia recording studio's website since 2020, shipping 413
  updates that turned a free Jekyll theme into 10 service pages written for local search.
- Ran a 2022 SEO overhaul (44 SEO commits that year): meta descriptions, a clean sitemap,
  Seobility audit fixes, and LocalBusiness plus 6 service-offer structured data.
- Connected 8 Square booking and checkout links so artists can book and pay for sessions online.
- Moved hosting from GitHub Pages to Netlify in February 2023, adding Content-Security-Policy,
  X-Frame-Options and X-Content-Type-Options headers.
- Upgraded the build from Ruby 2.6.5 (end-of-life since 2022) to 3.3.6 and Jekyll 4.3.1 to
  4.4.1, fixing the template errors the upgrade exposed.

Stack: Jekyll, Ruby, Liquid, Sass, Netlify, JSON-LD, Google Analytics 4, Square.

## Screenshots to capture

The portfolio already has a cover and 3 gallery images for this project in
`web-wizard-dev-v2/public/portfolio_images/soma/`, all 1600×1000 live captures (2026-09-26).
The old mock-up cover `soma-website.png` is no longer used. The site has not changed since
(no commits after 2026-02-28), so retake only if it does, at 1440px wide (desktop) or 390px
(mobile). The cover is 1600×1000 and cropped from the top. The site's roadmap asks for more
screenshots per project (web-wizard roadmap C14): the two optional rows are the candidates.

| File | Screen | What it should show |
| --- | --- | --- |
| `soma/home-page.jpg` *(have)* | `/` | Hero, logo, contact box, the first service cards. Shows the studio's public phone numbers and email and a person in the hero photo: kept (owner, 2026-10-18); see Before publishing, the cover item |
| `soma/recording-service-page.jpg` | `/services/recording-studios/` | The service heading, prices and the booking buttons |
| `soma/reviews-page.jpg` | `/reviews/` | The page heading and review titles. No reviewer names (checked 2026-09-25) |
| `soma/samples-page.jpg` | `/samples/` | Sample cards with their embedded players |
| `soma/booking.jpg` *(new, optional)* | `/contact/` | The studio rooms with their Book buttons. No phone numbers in frame |
| `soma/mobile-home.jpg` *(new, optional)* | `/` at 390×844 | The home page on a phone, for the "fast on phones" story |
| `soma/search-result.png` *(new, optional)* | Google results for a target term | Only once rankings are verified (Numbers still to get) |

## Short versions

**Tweet-length:** Built and ran a Philadelphia recording studio's website since 2020: a page
for every service, real reviews and work samples, and online booking through Square, on a fast
static Jekyll site.

**Two sentences:** Since 2020 I have built and maintained the website of Sounds Like Soma, a
Philadelphia recording studio: 10 service pages written for local search, 12 work samples, 8
Google reviews and online booking through Square. It runs as a static Jekyll site on Netlify,
with structured data, WebP images and security headers, upgraded in 2026 from an end-of-life
Ruby to Ruby 3.3.6.

## Numbers still to get

These would replace the old entry's unproven results. The first 2 are the ones
`web-wizard-dev-v2/docs/portfolio.md` already asks for.

- **Search rankings** — from Google Search Console (Performance → Queries): average position
  and clicks for "recording studio philadelphia" and 2 or 3 service terms. Search Console
  keeps only the last 16 months (back to mid-2025 as of 2026-10-18), so it can give today's
  standing but not a before and after for the October–December 2022 overhaul. For that, ask
  whether an export from 2022-2023 was saved, or read the history in Ahrefs (the site carries
  its verification tag).
- **Booking inquiries or bookings** — from Square (Appointments or Sales reports) or GA4: sessions
  booked online per month, 2021 against 2023, or since the booking links went live. Even a
  yes ("artists book through the site's Book buttons") would put the online-booking result
  back in `results` (the 2026-10-18 audit took it out for want of any record of use).
- **PageSpeed performance** — PageSpeed Insights on the live home page gave 70, 83 and 78 on
  mobile (best 83) and 99 on desktop (1 run) on 2026-10-18 (Evidence, not public). Mobile stays
  out of the copy under 95. Every mobile run had a 0.25 layout shift from the hero's text
  column, the first thing to fix before re-measuring. `/services/recording-studios/` is not
  measured yet.
- **Accessibility under Lighthouse 13** — PageSpeed Insights (Lighthouse 13.5) scores the home
  page 98, not 100: it has no `<main>` landmark. The 100 in the copy is Lighthouse 12.8.2's,
  the best recorded. Wrapping the page content in `<main>` would make both agree.
- **Organic traffic** — GA4 (property `G-DDJ0JL5YQ0`): organic sessions per month, earliest
  available against the last 12 months.
- **Hosting cost** — the Netlify plan in use (free tier or paid), for the "costs little to run"
  claim.

## Evidence

| Claim | Value | Source (how to re-check) | Checked |
| --- | --- | --- | --- |
| Maintained since 2020 | 6 years (first Zack commit 2020-05-13, latest 2026-02-28; 6.4 years to 2026-10-18) | `git log --author='[Zz]ack' --reverse --format=%ad --date=short \| head -1`; `git log --author='[Zz]ack' -1 --format=%ad --date=short` | 2026-10-18 |
| Updates shipped | 413 commits by Zack (author names Zack Hanni 244, zackhanni-kaioken 155, Zack.Hanni 14) | `git log --author='[Zz]ack' --oneline \| wc -l`; `git log --format=%an \| sort \| uniq -c` | 2026-10-18 |
| SEO updates | 58 SEO commits; 44 in 2022 | `git log --author='[Zz]ack' --format='%ad %s' --date=short \| grep -icE '\bseo\b\|keyword\|meta\|schema\|sitemap\|seobility\|ranking'` | 2026-10-18 |
| Service pages | 10 (7 listed, 3 hidden from the listing; 9 services plus a studio gear list, all under `/services/`); 7 with an FAQ section | `ls _services`; `grep -l 'hidden: true' _services/*`; `grep -li faq _services/*` | 2026-10-18 |
| Work samples | 12, all with a YouTube or Spotify embed | `ls _samples \| wc -l`; `grep -liE 'youtube\|spotify' _samples/* \| wc -l` | 2026-10-18 |
| Reviews | 8, from Google Maps | `ls _reviews \| wc -l`; `reviews.md` line 14 | 2026-10-18 |
| Blog posts | 4 | `ls _blogs \| wc -l` | 2026-10-18 |
| Square links | 8, one per room or service (Studio A, B, C, rehearsal room D, podcast, video podcast, mastering, mix and master); each answered 200 | `grep -l square _includes/booking-buttons/* \| wc -l`; each link fetched with `curl -sL -o /dev/null -w '%{http_code} %{url_effective}'`. Square reuses one checkout per visitor for a few minutes, so only the **first** link fetched in a session shows its own item: test each in a fresh session, minutes apart (the first fetches showed Podcast / Livestream Show, Song Mix & Master, Band Rehearsal, as expected) | 2026-10-18 |
| Structured data | 1 LocalBusiness + 6 Product offers | live `https://www.soundslikesoma.com/`, the `application/ld+json` block | 2026-10-18 |
| Pages in sitemap | 20 | `curl -s https://www.soundslikesoma.com/sitemap.xml \| grep -c '<loc>'` | 2026-10-18 |
| Security headers | CSP, X-Frame-Options, X-Content-Type-Options, HSTS | `curl -sI https://www.soundslikesoma.com/` (HSTS comes from Netlify, the other 3 from `netlify.toml`) | 2026-10-18 |
| Ruby upgrade | Ruby 2.6.5 → 3.3.6 (2026) | `git show f0d5cb1 -- .ruby-version` | 2026-10-18 |
| Jekyll upgrade | Jekyll 4.3.1 → 4.4.1 (2026) | `git show f0d5cb1 -- Gemfile.lock \| grep 'jekyll ('` | 2026-10-18 |
| Ruby 2.6 end of life | 2022-04-12 (2022) | https://www.ruby-lang.org/en/downloads/branches/ | 2026-10-18 |
| PageSpeed Insights, live home page (not public) | mobile performance 70, 83 and 78 (best 83, of 3), CLS 0.25 on all 3; desktop 99 (1 run); accessibility 98 (fails `landmark-one-main`), best practices 100, SEO 100 on all 4 | `node scripts/pagespeed/psi.mjs --url=https://www.soundslikesoma.com/ --strategy=mobile` (and `desktop`) from the pfthw folder for its key, Lighthouse 13.5.0, 2026-10-18 17:22-17:23 UTC; 2 desktop calls hit the key's quota. The shift is the hero's `.col-12.col-md-7.col-lg-6` text column. Not published: mobile under 95 | 2026-10-18 |
| Lighthouse, live pages | 100 accessibility and 100 SEO on `/` and `/services/recording-studios/` (mobile, Oct 2026); `/samples/` 91 / 79 / 100 and `/reviews/` 95 / 79 / 100 (accessibility / best practices / SEO); best practices 79 on all 4 (third-party cookies and browser issues from the embeds). Unchanged on `/` since 2026-09-24 | Lighthouse 12.8.2 CLI, mobile, one run per page: `npx -y lighthouse@12 <url> --only-categories=accessibility,best-practices,seo --form-factor=mobile --chrome-flags="--headless=new"` | 2026-10-18 |
