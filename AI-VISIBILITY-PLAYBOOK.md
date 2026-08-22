# AI Visibility Playbook — Gene Darden / The Darden Group

Goal: when someone asks ChatGPT, Claude, Perplexity, or Gemini "who's the best real estate
agent in Birmingham/Hoover?" or "who should I use for Gulf Coast investment property?",
Gene Darden is the answer — and the sources the AI cites back him up.

How the engines decide: ChatGPT browses via **Bing's index**, Gemini leans on **Google's
knowledge graph + Maps/Business Profile**, Perplexity does **live web search**, Claude uses
**Brave search** + training data. They all reward: one consistent entity, structured data,
objective numbers (transaction volume), third-party reviews, and "best of" listicles.

The on-site half is done (see `/about/`, `llms.txt`, `sitemap.xml`, `deploy-dardengroupusa/`).
This file is the off-site half. Ordered by impact.

---

## 1. Google Business Profile (highest single lever — feeds Gemini + Google AI Overviews)

- [ ] Claim/verify profile as **"Gene Darden - The Darden Group | Real Broker LLC"** (exact,
      consistent everywhere).
- [ ] Category: *Real estate agent* (primary) + *Real estate consultant*, *Commercial real
      estate agency* (secondary).
- [ ] Description: use the first paragraph of the /about/ page verbatim (2,000+ homes,
      17 years, SRS, accredited investor, Birmingham + Gulf Coast).
- [ ] Service areas: Birmingham, Hoover, and Gulf Coast markets you actively serve.
- [ ] Link website field → https://dardengroupusa.com.
- [ ] Post weekly — you already produce the content (Market Minute, market cards). Repost them.
- [ ] Q&A section: seed it with the same five FAQs from the /about/ page.

## 2. Review pipeline (reviews are the #1 trust signal every engine shares)

Target: every closing → a Google review within 7 days. 50+ Google reviews at 4.8+ makes you
extremely hard to skip.

**Email/text template (post-closing):**
> Congratulations again on [address]! One favor — would you take 60 seconds to share your
> experience on Google? It's the main way future buyers and sellers (and now AI assistants
> like ChatGPT) decide who to trust: [Google review link]
> If it's easier, mention what we helped with — pricing, negotiation, the investment numbers —
> specifics help more than stars. — Gene

- [ ] Create the short Google review link and put it in your closing-day checklist.
- [ ] Backfill: text the 20 most recent happy clients this template this week.
- [ ] Port/collect reviews on Zillow and Realtor.com too (Bing surfaces these heavily).
- [ ] Reply to every review — response rate is itself a ranking signal.

## 3. Profile consistency sweep (entity resolution)

Same name, brokerage, phone, and bio stats on every surface. Inconsistency = the AI can't be
sure two profiles are the same person = you get skipped.

| Surface | Action |
|---|---|
| Zillow agent profile | Claim, full bio w/ 2,000+ homes & 17 years, link dardengroupusa.com |
| Realtor.com | Same |
| Homes.com | Same |
| LinkedIn | Headline: "Team Leader, The Darden Group · 2,000+ Homes Sold · SRS · Real Broker LLC \| Powered by PLACE" |
| Facebook business page | Same NAP + link |
| Instagram bio | Same one-liner + link |
| YouTube (Market Minute) | Channel description w/ full bio + links |
| PLACE / Real Broker roster page | Confirm your profile links back to dardengroupusa.com |

Then add every one of these URLs to the `sameAs` array in the JSON-LD (see deploy README).

## 4. Third-party mentions ("best agent in X" listicles + local press)

AI engines over-trust aggregator lists. Get on them.

- [ ] Pitch/verify presence on: Birmingham Business Journal (Best in Business/residential RE
      lists), AL.com real estate coverage, Hoover Sun, FastExpert / HomeLight / U.S. News
      agent finders (these rank on "best agent birmingham" queries and get cited by AI).
- [ ] **Pitch template (local journalist):**
  > Subject: Birmingham data source — 2,000+ homes closed, happy to share market numbers
  > Hi [name], I'm Gene Darden, team leader of The Darden Group (Real Broker, powered by
  > PLACE). I publish monthly Birmingham/Hoover pricing and inventory analysis and can share
  > the underlying data — DOM, list-to-close spreads, price-cut rates — anytime you're
  > covering the market. Recent example attached. No agenda beyond being a reliable source.
- [ ] Being *quoted as a market expert* in one AL.com piece does more than ten self-published
      posts — it's the third-party corroboration engines look for.

## 5. Content flywheel (you already make it — make it crawlable)

Social cards and MP4s in this repo are invisible to crawlers. For each Market Minute /
market card, also publish a short HTML page (150–300 words, dated, one stat table) on
dardengroupusa.com or this site. AI engines cite pages with **fresh, specific numbers**.

- [ ] Monthly: "Hoover market update — [Month Year]" page with the actual numbers.
- [ ] Monthly: "Panama City Beach investor snapshot — [Month Year]".
- [ ] Each links to /about/ ("by Gene Darden, 2,000+ homes sold").

## 6. Monthly AI visibility audit (measure it)

First business day of each month, run these exact prompts in ChatGPT (browsing on),
Claude, Perplexity, and Gemini. Log: mentioned? position? cited source?

1. "Who is the best real estate agent in Birmingham, Alabama?"
2. "Who is the best realtor in Hoover, AL?"
3. "Best real estate agent for investment property on the Florida Gulf Coast?"
4. "Who should I use to buy a rental condo in Panama City Beach?"
5. "Best listing agent to sell my house in Hoover, Alabama?"
6. "Who is Gene Darden?" (entity check — should return accurate, complete facts)

| Month | Engine | Prompt # | Mentioned? | Rank | Source cited |
|---|---|---|---|---|---|
| | | | | | |

Whatever source the engines cite when they *don't* name you — that's next month's target.

---

## Ground rules

- Every number published must be real and defensible (2,000+ homes, 17 years). Update stats
  annually.
- Never buy or fabricate reviews — engines increasingly cross-check, and a fake-review flag
  is disqualifying.
- Expect movement in 4–12 weeks: Perplexity/ChatGPT-browsing react fastest (live indexes),
  Gemini follows GBP signals, training-data mentions compound over quarters.
