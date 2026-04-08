# kamo-2-results

Static viewer for HumanVid validation inferences.

**Live:** https://git-kinetix.github.io/kamo-2-results/

This repo contains only the HTML/JS for a video gallery. The videos themselves
are hosted on a public CDN — the pages just fetch a small `manifest.json` and
embed each video as an HTML5 `<video>` element with autoplay-on-scroll.

## Pages

| Path | Contents |
|---|---|
| `index.html` | 720p inferences (30 steps, drop@22, first_frame + face ref) |
| `native_480p/` | 480p native inferences (15 steps, default sampling) |

## Local development

```bash
python3 -m http.server 8090
# then open http://localhost:8090/
```

No backend, no build step, no dependencies — just static HTML, vanilla JS, and a
fetch to the public manifest.
