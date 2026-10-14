# App store search

Use for the Apple App Store and Google Play. These stores do not read the website title as the app title.

Official references change. Check the current limits in App Store Connect and Play Console before telling the user to cut or pad a field. As of the last stable public limits:

- Apple app name: 30 characters
- Apple subtitle: 30 characters
- Apple keyword field: 100 characters, comma-separated, no spaces required
- Google Play title: 30 characters
- Google Play short description: 80 characters

If a console shows a different limit, the console wins.

## Apple

- The name and subtitle are indexed and shown. Put the distinguishing function there if it fits and still reads like a name.
- The keyword field is indexed and not shown. Do not repeat words already in the name or subtitle. Apple combines them. Repeating wastes the 100 characters.
- Separate keywords with commas. Do not waste characters on spaces or on "app".
- Do not include competitor names, irrelevant celebrity terms, or trademarks you do not have rights to use.
- Screenshots and the preview video sell the click. The first two screenshots matter most. They should show the product, not a slogan that could belong to any app.
- Ratings come from people who use the app. Do not prompt in a way that filters out unhappy users, and do not incentivize reviews against store rules.
- Localization is a different storefront. A keyword that works in US English may be wrong in another locale. Translate the intent, do not machine-pad the keyword field.

## Google Play

- Title, short description, and long description are all indexed. Write the short description for a person, because it is shown.
- The long description can cover real features. Repeating one keyword is stuffing, and Play has rejected listings for it.
- Google Play has no hidden keyword field equivalent to Apple's. Do not invent one.
- Screenshots, the feature graphic, and the video are conversion assets. A store listing experiment is the way to test them, not a guess.

## What to measure

Use the store's own acquisition report: impressions, page views, installs, and conversion by query or by referrer where the console shows it. Do not promise a rank from a keyword tool that scrapes the store. Those tools are hypotheses.

Do not claim a fixed share of downloads comes from search. The share depends on the app, the category, and paid spend. Read this app's report.

## Website

An app landing page can rank in Google. That is web SEO, not ASO. Use `references/seo-foundation.md` for that page, and SoftwareApplication markup only if the page shows the app facts the markup claims.
