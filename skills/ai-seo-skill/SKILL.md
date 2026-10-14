---
name: ai-seo-skill
description: >
  Use when the user wants a page, product, listing, or brand found in a search
  engine or search platform: Google, Bing, YouTube, Maps, Lens, TikTok,
  Instagram, Pinterest, LinkedIn, app stores, podcast apps, Amazon, or Walmart.
  Covers technical SEO, snippets, entities, topic clusters, local listings,
  video, visual search, Google AI Overviews, app-store search, audio search,
  and marketplace search. Trigger on rankings, schema, Core Web Vitals,
  backlinks, meta tags, local SEO, featured snippets, and YouTube or marketplace
  optimization. Do not use for citations inside ChatGPT or Perplexity, email,
  paid ads, analytics setup, or conversion-rate optimization.
license: MIT
compatibility: Any agent that loads Agent Skills. No account, package, or server required. Fetch the user's URL when a tool is available.
metadata:
  author: Byte Forward
  version: "1.0.0"
---

# Search visibility

Help a page, listing, or brand get found on the search surface the user actually cares about. Do not run a 13-discipline audit unless the question needs one.

## Scope

This skill covers surfaces where a person types, speaks, or points a camera to find something:

- Web: Google, Bing
- Answers on those engines: featured snippets, People Also Ask, AI Overviews
- Local: Google Business Profile, Apple Business Connect, Bing Places
- Video and social: YouTube, TikTok, Instagram, Pinterest, LinkedIn
- Visual: Google Lens and image search
- Apps: Apple App Store, Google Play
- Audio: Apple Podcasts, Spotify, and crawlable transcripts
- Marketplaces: Amazon, Walmart

Out of scope: getting cited by ChatGPT or Perplexity, email, paid ads, analytics implementation, and conversion-rate optimization. Say so and stop. Do not invent a companion skill and pretend it is installed.

## Before answering

1. Name the surface. "SEO" is not a surface. Google web, Maps, YouTube, Amazon, and the App Store do not share one algorithm.
2. Name the business type if it changes the plan. If the URL, market, or business type is missing and the answer would change, ask one focused question. Do not ask if the request is already specific.
3. If a URL is available and you can fetch it, inspect the page. Do not audit a domain from its name.
4. Load only the one or two files below that match the question. Do not load the rest.
5. Produce a scorecard, schema package, or 90-day plan only when the user asked for that deliverable. Load `references/deliverables.md` for the format.

| Question | Load |
| --- | --- |
| Crawl, index, speed, titles, links, keywords | `references/seo-foundation.md` |
| Snippets, People Also Ask, voice, AI Overviews | `references/answers.md` |
| Knowledge Graph, schema identity, topic clusters | `references/entities.md` |
| Maps, Business Profile, citations, reviews | `references/local.md` |
| TikTok, Instagram, Pinterest, LinkedIn, YouTube | `references/social-video.md` |
| Google Lens, image search, alt text | `references/visual.md` |
| App Store or Google Play | `references/aso.md` |
| Podcasts, Spotify, transcripts | `references/audio.md` |
| Amazon or Walmart listings | `references/marketplace.md` |
| A requested audit, plan, or schema package | `references/deliverables.md` |

## Rules that override the old habits

- Do not invent a percentage, study, or "industry benchmark." If a number is not in the loaded reference and tied to a primary source, leave it out.
- Separate three labels: **platform requirement**, **documented platform guidance**, and **industry practice**. Do not present the third as the first.
- For Google web search, follow [Google's generative AI guide](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide). Those features use the same ranking systems as Search. There is no special schema to add. Do not prescribe chunk lengths, entity-density targets, or an `llms.txt` file. Google says those tactics can be ignored.
- Do not recommend HowTo rich results. Google removed them. The FAQ rich-result docs now redirect to the removal note: FAQ rich results were limited to authoritative government and health sites, and unused FAQ markup has no visible effect in Google Search. A real FAQ can still help a reader. Do not promise a rich result.
- `Speakable` is a beta news feature for US English Assistant playback, about 20 to 30 seconds. It is not a general voice-ranking tactic.
- You cannot mark a page as a featured snippet. Google decides. Write a direct answer because the searcher needs it, not because a word-count formula wins position zero.
- Do not apply one checklist to every URL. A contact page, a product page, and a guide do not need the same blocks.
- Do not recommend review gating, fake reviews, keyword stuffing, doorway pages, cloaking, hidden text, or schema that describes content the page does not show.
- Do not tell the user to track rankings on a platform that does not expose them. Say which metric that platform actually shows.
- A title that reads like a keyword list is a defect, not an optimization.

## What to prioritize

Start from the business, not from a fixed stack.

| Business | Start here | Add if the evidence supports it | Usually ignore at first |
| --- | --- | --- | --- |
| Local service | Web SEO, Business Profile | Snippets for question queries, entity consistency | App stores, marketplaces |
| SaaS or B2B | Web SEO, topic coverage, clear product pages | Video, entity markup | Marketplaces, podcasts |
| Store or DTC | Web SEO, product data, images | Marketplace listings, social search, video | App stores, unless there is an app |
| Professional service | Web SEO, entity clarity, useful explainers | Video | Marketplaces, app stores |
| Healthcare | Web SEO, local profile, careful claims | Question-style pages | Social as a search engine, unless the audience is there |
| Publisher | Web SEO, internal links, freshness | Social and video distribution | App stores, marketplaces |
| Hospitality | Web SEO, local profile, photos | Visual and social search | App stores, podcasts |
| Education | Web SEO, course or article structure | Video | Marketplaces |

Voice search is not a default priority. Spoken queries matter when the audience asks them. Do not cite a claim that half of all searches are voice. That figure is a misquoted forecast, not a current measurement.

## If they want a plan

Only then, sequence the work:

1. Make the important URLs crawlable, indexable, fast enough, and about one clear subject.
2. Fix the page the searcher lands on: title, heading, answer, internal links, and matching schema.
3. Expand to the next surface only after the first one is measurable.
4. Read the platform's own report before changing strategy. Search Console for Google. The native analytics for YouTube, a marketplace, or an app store.

## How to answer

Lead with the surface and the finding. Then:

- What is established from the page or the platform docs
- What is industry practice, labeled as such
- What you could not check
- The next change that would move the result, not a list of every discipline

Do not pad a title-tag question into a quarterly program.
