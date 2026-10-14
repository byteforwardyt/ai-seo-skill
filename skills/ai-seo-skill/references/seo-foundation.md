# Web search foundation

Use for Google and Bing organic search: crawl, index, titles, internal links, and page experience. Primary docs:

- https://developers.google.com/search/docs/fundamentals/seo-starter-guide
- https://developers.google.com/search/docs/appearance/core-web-vitals
- https://web.dev/articles/vitals
- https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls

## Check these before advising content

A page that is blocked, duplicated, or not indexed cannot be optimized into a ranking.

- `robots.txt` is not blocking the URL or its required resources.
- The page does not have `noindex` unless that is intentional.
- One canonical URL is declared, and the canonical is the URL you want indexed. Do not canonical a page to a different page and then expect both to rank.
- The URL is in an XML sitemap only if it is the canonical, indexable URL. A sitemap is a hint, not a ranking boost.
- Internal links use crawlable `<a href>` links. Buttons that only run JavaScript are not reliable links.
- The mobile version is the version Google indexes. If the mobile page hides the content, the desktop page does not save it.
- Important content is in the HTML response, or rendered JavaScript that Google can fetch. Do not assume a client-side app is indexed because it looks fine in a browser.

## Core Web Vitals

Google's current Core Web Vitals, measured at the 75th percentile of real users, separately for mobile and desktop:

- LCP within 2.5 seconds
- INP within 200 milliseconds
- CLS of 0.1 or less

FID is retired. Do not report it. Lab scores are a hint. Field data in Search Console or CrUX is the measurement that matters. A failing vital is a page-experience problem, not proof that rankings will jump if it turns green.

## Titles and snippets

- The title should say what the page is, in the searcher's language. Put the distinguishing words where a person will see them. Do not front-load a keyword if that makes the title nonsense.
- Google rewrites titles. A unique, specific title is more likely to survive than a template that repeats the brand and the same modifier on every URL.
- The meta description is a snippet candidate, not a ranking field. Write it for the click. Stay near the length Google can show, and expect rewrites.
- One H1 that matches the page's subject. Subheadings should mark real sections, not a keyword list.
- The URL slug can be short and readable. Changing a URL that already ranks requires a redirect. Do not change slugs for style.

## Links

- Link to related pages when the link helps the reader move. Three links is not a quota, and a page with no internal links is a dead end.
- Outbound links to primary sources are fine. Do not add them to satisfy a count.
- Broken internal links and redirect chains are technical defects. Fix those before chasing new backlinks.
- Backlinks are a result of being worth citing. Do not recommend buying links, private blog networks, or mass guest-post schemes.

## Keywords

Start from the query the page should satisfy, the page that already ranks for it, and the words the page actually uses. A keyword tool is a hypothesis source. It is not evidence that this site should target that query.

One page, one primary subject. Do not create a near-duplicate URL for every phrasing of the same question. Google's generative AI guide says query fan-out already looks for related wording, and that separate pages for every variation are a temptation to resist.

## What not to claim

Do not say a title length, a keyword density, or a link count will produce a ranking. Say what is wrong on this page and what to change.
