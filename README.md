# jesseweb.com

**[jesseweb.com](https://jesseweb.com)** is an interactive 1950s television set that broadcasts my resume. Turn on the WJMT-TV "Tele·Torres 4000", surf 22 channels of real vintage footage, and watch the newsprint TV Programs guide fill in my career as the shows air.

## How it works

- **One broadcast reel.** All 101 shows and 6 station bumpers live in a single 24-minute MP4. Changing channels is just a seek, which browsers never block, so audio and video always play. No-repeat shuffle bags make sure you never see the same show twice until a channel's whole lineup has aired.
- **Real CRT physics.** The picture, station idents, closed captions, scanlines, and static are composited on a 2D canvas, then warped together through a WebGL barrel-distortion shader and clipped to a pillow-shaped tube. The floor reflection is the same frames mirrored, faded, and blurred onto the floorboards.
- **Vintage footage only.** Every clip was cut from verified public-domain sources on the Internet Archive (Prelinger Archives and friends), normalized to 240x180, loudness-leveled, and reviewed frame by frame before making the schedule.
- **No frameworks, no build.** One static HTML file plus the reel. Works in Firefox, Chrome, and Safari, on desktop and phones.

## Layout

| Path | What it is |
| :-- | :-- |
| `site/index.html` | The entire application: markup, CSS, WebGL shaders, broadcast state machine |
| `site/reel.mp4` | The broadcast reel: 107 segments, 23.9 minutes, 240x180 |

## Deploy

Hosted on Cloudflare Pages:

```sh
npx wrangler pages deploy site --project-name jesseweb
```

## License

Code is MIT licensed. All footage is public domain, sourced from the [Internet Archive](https://archive.org), largely the [Prelinger Archives](https://archive.org/details/prelinger).
