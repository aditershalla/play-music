# Play Music — personal audio-only radio player

A personal listening website with three permanent station presets: **Play Mix**, **Play Gold**, and **Play Lounge**, plus the seasonal **Play Xmas**.

## Latest version

The former YouTube video drawer has been removed completely from the website. The fixed bottom player now uses one native HTML5 audio element with:

- Play / pause and stop
- Station switching without a page refresh
- Volume and mute controls
- Audio status indicator
- Audio file picker per station
- Direct HTTPS audio stream URL per station (MP3, AAC, OGG or another format supported by the browser)

### Setting up your own audio source

At the **My audio sources** section, either:

1. Paste an **HTTPS direct audio-stream URL** for a station, then press **Save**; or
2. Choose your own MP3/M4A/audio file using the file picker for that station.

Click the station's **Listen** button or select the station from **Choose Radio** at the bottom.

Stream URLs are saved in your browser's local storage and aren't shared across devices. Local files stay in the current browser session only. They are *not* uploaded to GitHub or Cloudflare. No default audio stream is configured until you provide one.

**Important:** The original Play Lounge source was a YouTube video (`9UMxZofMNbA`). YouTube's embedded-player policies don't permit using hidden-video audio playback. This source is no longer used by the new audio-only player. You can still listen to it on YouTube separately, or supply a legitimate direct radio audio stream instead. Personal use doesn't remove the YouTube player restrictions.

## Cloudflare Pages

The website is static and is deployed from the repository root (branch `main`) without a build command.

- File: `index.html`
- Framework preset: None
- Build command: blank
- Output directory: repository root

After a push to GitHub, Cloudflare Pages should automatically deploy if Git integration is configured.

## Privacy

The GitHub repository and any unprotected Cloudflare Pages URL are public. The noindex tag and robots.txt are requests to search engines, **not access control**. Use Cloudflare Access or another authentication mechanism for a private website.

## Music rights

Use music and audio streams you're allowed to access. Do not extract YouTube audio or rebroadcast a copyrighted stream without permission.
