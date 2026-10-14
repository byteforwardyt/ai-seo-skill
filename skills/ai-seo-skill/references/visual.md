# Visual search

Use for Google Images, Google Lens, and similar camera search. Primary docs:

- https://developers.google.com/search/docs/appearance/google-images
- https://developers.google.com/search/docs/appearance/structured-data/image-license-metadata
- https://developers.google.com/search/docs/crawling-indexing/sitemaps/image-sitemaps

## What the image needs

Lens and image search use the picture plus the page around it. A perfect alt attribute cannot rescue an image that does not show the thing, or a page that is about something else.

- The image should depict the subject. A decorative stock photo of a handshake does not help a search for a product.
- Alt text describes the image for someone who cannot see it. Include the product or place name when that is what the image shows. Do not stuff a keyword list into alt text.
- A nearby caption and heading should agree with the image. Lens uses surrounding text.
- File name can be readable (`blue-wool-coat.jpg`). It is a hint, not a field to stuff.
- Use a supported format and a size that is sharp on a phone. A huge uncompressed file is a speed problem. A tiny blurry file is a Lens problem.
- Do not block the image in `robots.txt` if you want it indexed. Do not lazy-load it in a way that never puts the URL in the HTML.

## Structured data and sitemaps

Add image sitemap entries or `ImageObject` metadata for images you need discovered, especially if they are loaded in a way Google might miss. License and creator metadata belong on images where the license matters. They are not a ranking boost for a product photo.

Product images on a product page should match the Product markup. The image in the markup must be the image on the page.

## Pinterest Lens

A pin image has to work as a standalone picture. See `references/social-video.md`. Do not assume a Google Images fix changes Pinterest.

## What not to claim

Do not quote a monthly Lens search volume. Google has described Lens use in billions at various times, and the number is not a tactic. Describe the image and the page, then stop.
