# Deliverables

Load this only when the user asked for an audit, a plan, a content brief, or schema. Do not attach one of these to a narrow question.

Score only what was observed. `Not checked` is a valid result. Do not fill a gap with a benchmark.

## Audit

```text
Surface:
URL or listing:
Business type:

Established
- ...

Inferred
- ...

Not checked
- ...

Fixes, in order
1. ...
```

For a multi-surface audit, repeat that block per surface. Do not score a surface you did not inspect. Do not add a numeric grade unless the user asked for one, and if they did, define the scale from the checks you ran.

## 90-day plan

Use only on request. Four lines per month is enough.

```text
Month 1: make the primary surface crawlable, accurate, and measurable
- ...
Month 2: fix the pages or listings that already get impressions
- ...
Month 3: add the next surface only if month 1 has a report to read
- ...
Do not do yet:
- ...
```

## Content brief

```text
Query the page should satisfy:
Searcher need:
Page type:
Must include:
Must not include:
Internal links to add:
Schema type, if the page will visibly support it:
How we will know it worked:
```

The brief is for a writer. It is not a keyword-density sheet.

## Schema package

Give JSON-LD only for a type the page will visibly support. Use placeholders the user must replace. Validate against the current Google rich-result docs or schema.org before telling them to ship it.

Organization example, for a page that shows this identity:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "REPLACE",
  "url": "https://example.com/",
  "logo": "https://example.com/logo.png",
  "sameAs": ["https://www.wikidata.org/wiki/REPLACE"]
}
</script>
```

LocalBusiness example, for a page that shows this location:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "REPLACE",
  "url": "https://example.com/locations/REPLACE",
  "telephone": "REPLACE",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "REPLACE",
    "addressLocality": "REPLACE",
    "addressRegion": "REPLACE",
    "postalCode": "REPLACE",
    "addressCountry": "REPLACE"
  }
}
</script>
```

Do not include `HowTo`. Do not include `FAQPage` as a rich-result tactic. Do not include a rating the page does not display.
