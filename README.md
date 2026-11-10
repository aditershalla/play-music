# Play Music

A personal home-listening website with three year-round station presets: Play Gold, Play Mix, and Play Lounge. Play Xmas appears seasonally. The site plays videos through YouTube's **official, visible embed** where the original creator allows embedding.

## Current status

- `index.html` is a standalone first deployment version. It can be deployed as a static website without a build step.
- Play Lounge initially points to YouTube video `9UMxZofMNbA` supplied by the project owner.
- Gold, Mix and Xmas YouTube links are configurable in the **My YouTube streams** section.
- Links are stored in your browser's `localStorage`, not synchronized between devices.
- If a creator disables embedding, use **Open on YouTube**. The website does not extract or restream audio.
- No public live station streams, audio hosting, or AzuraCast server are included in this single-file edition.

## Cloudflare Pages deployment

1. Open Cloudflare dashboard → Workers & Pages → Create application → Pages → Connect to Git.
2. Select GitHub repository `aditershalla/play-music` (branch `main`).
3. Select a static site/no framework preset; **no build command**; use the repository root as output directory if supported. The file `index.html` is at the root.
4. Deploy. Select a different Pages project name if `play-music` is already taken.
5. If personal/private use is intended, configure **Cloudflare Access** before sharing the Pages URL. `noindex` is not an access control.

## Rights and privacy

Use this as a personal listening hub. YouTube content belongs to the respective creators. Never use a downloaded YouTube audio stream as your own rebroadcast without necessary permissions. This GitHub repository is currently **public**; do not commit passwords, API keys, or private data.
