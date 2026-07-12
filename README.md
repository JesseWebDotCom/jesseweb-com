# jesseweb.com

**[jesseweb.com](https://jesseweb.com)** is one resume told by two machines. Pick the television: a 1950s WJMT-TV set that broadcasts 22 channels of real vintage footage while a newsprint TV guide fills in my career. Or pick the arcade: Torres Quest, a full side-scrolling platformer through six eras of my life, framed as a 90s VHS home video, with a helicopter flight, a company car, a wedding, a band, an underground tunnel, era-true music, and an AGI boss fight that ends in fireworks.

## How it works

- **One broadcast reel.** All 101 shows and 6 station bumpers live in a single 24-minute MP4. Changing channels is just a seek, which browsers never block, so audio and video always play. No-repeat shuffle bags make sure you never see the same show twice until a channel's whole lineup has aired.
- **Real CRT physics.** The picture, station idents, closed captions, scanlines, and static are composited on a 2D canvas, then warped together through a WebGL barrel-distortion shader and clipped to a pillow-shaped tube. The floor reflection is the same frames mirrored, faded, and blurred onto the floorboards.
- **Vintage footage only.** Every clip was cut from verified public-domain sources on the Internet Archive (Prelinger Archives and friends), normalized to 240x180, loudness-leveled, and reviewed frame by frame before making the schedule.
- **No frameworks, no build.** One static HTML file plus the reel. Works in Firefox, Chrome, and Safari, on desktop and phones.

## Layout

| Path | What it is |
| :-- | :-- |
| `site/index.html` | The front page: pick the television or the arcade |
| `site/tv/index.html` | The television: markup, CSS, WebGL CRT shader, broadcast state machine |
| `site/tv/reel.mp4` | The broadcast reel: 107 segments, 23.9 minutes, 240x180 |
| `site/game/index.html` | Torres Quest: a complete canvas platformer in one file |

## Deploy

Hosted on Cloudflare Pages:

```sh
npx wrangler pages deploy site --project-name jesseweb
```

## License

Code is MIT licensed. All footage is public domain, sourced from the [Internet Archive](https://archive.org), largely the [Prelinger Archives](https://archive.org/details/prelinger).
