# Snippets, voice, and AI Overviews

Use when the question is featured snippets, People Also Ask, spoken queries, or Google's generative search features.

Primary docs:

- https://developers.google.com/search/docs/appearance/featured-snippets
- https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
- https://developers.google.com/search/docs/appearance/ai-features
- https://developers.google.com/search/blog/2023/08/howto-faq-changes
- https://developers.google.com/search/docs/appearance/structured-data/speakable

## Featured snippets

Google decides whether a page becomes a featured snippet. There is no markup that requests one. A click on a snippet jumps to the matching section when Google can find it.

Write the answer because the query is a question:

- Put the direct answer near the heading that asks the question.
- Use a short paragraph, a list, or a table when that format matches the question. A list for a list question. A definition for a "what is" question. Do not add a 40-to-60-word block after every heading.
- Keep the answer self-contained. A snippet that only makes sense with the previous paragraph is a bad snippet and a bad paragraph.
- To opt out, use `nosnippet`, `data-nosnippet`, or a short enough `max-snippet`. Google does not publish an exact minimum length that guarantees exclusion. `max-snippet` is an experiment, not a guarantee. `nosnippet` is the reliable opt-out, and it also removes the regular snippet.

## People Also Ask and on-page questions

Add a question only if searchers ask it and the page can answer it honestly. Three to five filler questions do not create a feature. If the questions are real, visible FAQ text helps the reader. It is not a rich-result strategy.

Google limited FAQ rich results in August 2023 to well-known authoritative government and health sites, and the FAQ rich-result documentation now redirects to that removal note. Unused FAQ markup does not hurt Search and also has no visible effect. Do not tell a normal business to add `FAQPage` so it can win a rich result.

Do not recommend `HowTo` rich results. Google removed them from mobile and then from desktop, and dropped the How-to search appearance.

## Voice

Spoken queries are usually longer and more conversational than typed queries. That is a writing observation, not a market-share statistic. Do not say that half of searches are voice.

If the audience uses a speaker or a phone assistant, answer in one or two sentences a person could hear, then give the detail. Do not add `Speakable` unless the page is English news content aimed at US Google Assistant playback. That feature is beta, currently for that case, and Google recommends about 20 to 30 seconds of marked text. It is not a ranking switch.

## Google AI Overviews and AI Mode

Google's own guide says these features are rooted in core Search ranking systems. From Google's perspective, optimizing for them is SEO. Their terms for the vendor labels: "AEO" and "GEO" are names other people use; Google does not require a separate program.

Documented guidance to follow:

- The page must be indexed and eligible to appear in Search. A blocked page cannot be cited.
- Unique, firsthand, non-commodity content matters more than a formatting trick. A summary of what other pages already say is commodity content.
- Do not create a separate URL for every phrasing of the same question.
- There is no special schema.org type to add for AI Overviews. Eligible structured data for a real visible feature is still worth adding. Invented "AI schema" is not.
- Do not recommend chunk-length targets, entity-density targets, or an `llms.txt` file. Google's guide says those tactics can be ignored.
- Do not recommend writing for a model instead of a reader. If generative tools help draft, the page still has to be accurate, original, and useful to a person.
- Measure with Search Console, not with a vendor dashboard you have not seen.

Do not quote a percentage of searches that show AI Overviews, a citation-lift percentage, or a word-count window. Those figures move, conflict, and are usually vendor studies. If the user supplies a study, name the publisher and the date, and do not treat it as a rule.

## Bing

Bing has its own index and its own webmaster tools. Do not assume a Google fix changes Bing. Submit the sitemap in Bing Webmaster Tools if that property is unverified. Do not claim a fixed overlap between Bing results and any chat product.
