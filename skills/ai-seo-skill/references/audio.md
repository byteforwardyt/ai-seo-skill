# Podcast and audio search

Use for Apple Podcasts, Spotify, and episode pages that Google can index.

## The show record

Directories search the fields you submit in the RSS feed and the show dashboard.

- Show title: the name a person would type. Do not append a keyword slogan to the title if the directory shows that title everywhere.
- Show description: what the show is, who it is for, and what a typical episode covers.
- Category: the closest true category. A wrong category puts the show in the wrong browse path.
- Author, owner email, language, and explicit flag should be accurate. A missing owner email is an operational defect, not a ranking trick.
- Artwork must meet the directory's current size and the safe-area rules. Check Apple and Spotify's current specs before exporting. Do not guess the pixel size from memory if you can open the spec.

## Episodes

- Episode title: the topic, specific enough to choose. Season and episode numbers do not help a searcher who types a question.
- Episode description: the question the episode answers, the guest's real name, and any products or books mentioned if a person might search those.
- Chapters and show notes, when the host supports them, help a listener. They also give a crawlable page something true to index.

## Google

Apple and Spotify do not give their index to Google. If the episode should be findable in Google, publish a crawlable page with the title, description, and a transcript or substantial show notes. A player embed with no text is a thin page.

The transcript should match the episode. A generated transcript full of wrong names is worse than no transcript. Correct names before publishing.

Video episodes that also live on YouTube follow `references/social-video.md` as well.

## What not to claim

Do not say audio is "increasingly indexed" as if that were a measured trend you can act on. Say which directory field is empty, and whether a crawlable transcript exists.
