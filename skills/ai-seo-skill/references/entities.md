# Entities and topic coverage

Use when the question is brand identity in search, structured data, or whether the site covers a subject or just a keyword.

Primary docs:

- https://developers.google.com/search/docs/appearance/structured-data/organization
- https://developers.google.com/search/docs/appearance/structured-data/local-business
- https://developers.google.com/search/docs/appearance/site-names
- https://schema.org/docs/documents.html

## Identity

A search engine can only treat a brand as one thing if the site, the profiles, and the markup describe the same thing.

- Use one name, and use it the same way in the title, the logo alt text, the Organization or LocalBusiness markup, and the profiles you control.
- Organization or LocalBusiness markup must match visible content. Do not mark up a business the page does not identify.
- `sameAs` should point at profiles the business actually owns: the official site, Wikidata if a sourced item exists, and the real social or directory profiles. Do not create a Wikidata item stuffed with promotional claims. Wikidata has notability rules, and a rejected item does not help.
- NAP for a local business means name, address, and phone. They should match the Business Profile. A virtual office that the business does not occupy is a false address.
- Site name markup helps Google show the right name. It does not create a Knowledge Panel. Panels are generated, not requested.

## Structured data that is still worth adding

Add the type that describes the visible page, and validate it:

- Organization or LocalBusiness on the page that identifies the business
- Article on an article, with a real author and a real date
- Product or merchant listing on a product page, including the price and availability the page shows
- Breadcrumb when the site has a visible hierarchy
- VideoObject when the page embeds a video
- Review snippet only for a review the page actually contains, from a person who is not the business reviewing itself

Skip types Google no longer shows as rich results. `HowTo` is one. `FAQPage` is not a general rich-result lever. See `references/answers.md`.

Markup that contradicts the page can be treated as spam. If the price, rating, or author is not on the page, do not put it in JSON-LD.

## Topic coverage

Cover a subject by answering the distinct questions a searcher has, and link those pages together when the link is useful. That is the practical version of a topic cluster.

- One pillar page that states the subject and links to the specific pages.
- Supporting pages that each answer a different question. Merge pages that target the same question with different wording.
- Internal links should use the words a reader would click, not an exact-match keyword on every link.
- Do not build a cluster for a subject the business cannot speak about from experience. Thin pages created to look complete are worse than a gap.

Entity-attribute-value mapping is a way to list what a searcher needs to know about a thing: what it is, who it is for, what it costs, how it compares. Use it to find missing sections. Do not turn it into a density target. There is no legitimate "entities per 1,000 words" quota.

## What you cannot promise

Markup does not put a brand in the Knowledge Graph. Consistent, corroborated identity makes that possible. Say that, and stop.
