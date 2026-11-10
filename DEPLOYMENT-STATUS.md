# Play Music deployment checklist

## Confirmed
- Main static site: `index.html`.
- YouTube source for Play Lounge: `9UMxZofMNbA`.
- Three permanent station presets and a seasonal Play Xmas.
- Configurable YouTube links saved per browser.
- Static privacy headers and `robots.txt`.
- CI checks for required files and JavaScript syntax.

## Check in Cloudflare
1. Workers & Pages → Pages → `play-music` → Deployments.
2. Confirm most recent `main` deployment is marked **Success**.
3. Open the **exact** production URL shown by Cloudflare (do not assume the name).
4. Verify homepage, station selection, and YouTube **Open on YouTube** fallback.
5. For private access, protect the site through Cloudflare Zero Trust → Access → Applications → Add application → Self-hosted; configure your own permitted email identity. Robots.txt/noindex are not access controls.

## Limits
- Embedded YouTube playback depends on third-party embed permissions and browser restrictions.
- Audio is not extracted or rebroadcast.
- The current code includes only one preconfigured YouTube source. Gold, Mix and Xmas need selected source URLs.
- Publishing to a `pages.dev` hostname makes it publicly accessible until Cloudflare Access is configured.
