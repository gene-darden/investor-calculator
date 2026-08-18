# Deploying the AI-visibility package to dardengroupusa.com

This folder is a ready-to-upload kit. dardengroupusa.com is the **canonical home** for the
"Gene Darden" entity — every other property (mysrsagent.com, GitHub Pages, social profiles)
should link back to it.

## Steps

1. **About page** — Publish `about-gene-darden.html` at `https://dardengroupusa.com/about/`
   (i.e., as `about/index.html`). If your site builder (Wix/Squarespace/WordPress/kvCORE etc.)
   can't take raw HTML pages, recreate the visible content on a page named "About Gene Darden"
   and paste the two `<script type="application/ld+json">` blocks into the page's
   custom-code/head-injection slot.
2. **robots.txt** — Upload `robots.txt` to the domain root. If the platform manages robots.txt
   for you, just confirm it does NOT block GPTBot, ClaudeBot, PerplexityBot, or Google-Extended.
3. **llms.txt** — Upload `llms.txt` to the domain root (`https://dardengroupusa.com/llms.txt`).
4. **Sitemap** — Ensure the platform emits a sitemap at `/sitemap.xml` that includes the new
   /about/ page, then submit it in Google Search Console and Bing Webmaster Tools.
   **Bing matters more than usual: ChatGPT's browsing runs on Bing's index.**
5. **Homepage schema** — Add the RealEstateAgent JSON-LD (copy the first `<script
   type="application/ld+json">` block from `about-gene-darden.html`) to the homepage head too.
6. **mysrsagent.com** — Add one line to its footer or about section linking to
   `https://dardengroupusa.com/about/` ("Gene Darden · The Darden Group") so the entity web
   is bidirectional.

## Fill in before/after publishing

- **Social profiles**: add your real profile URLs to the `sameAs` array in the JSON-LD —
  Zillow agent profile, Realtor.com profile, LinkedIn, Instagram, Facebook business page,
  YouTube. Every verified profile added strengthens entity confidence for AI models.
- **License number**: add your AL (and FL, if applicable) license number to the page footer
  and as an additional `hasCredential` entry — it's an unambiguous identity signal.
- **Reviews**: once your Google Business Profile has reviews, add an `aggregateRating`
  property to the RealEstateAgent JSON-LD with the real count and average. Never publish
  ratings that don't exist on a verifiable third-party surface.

## Validate

- https://validator.schema.org — paste the page URL, confirm zero errors.
- https://search.google.com/test/rich-results — confirm FAQ rich result eligibility.
