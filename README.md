# idezign-com

iDezign.com — the hardware side of iDezign Technology. Hands-on IT, networking, and systems work in Redding, California — since 1997.

Sister site: [idezign.ai](https://idezign.ai) (the AI consulting arm) · repo: [idezigntech/idezign-site](https://github.com/idezigntech/idezign-site)

## Stack

Static HTML, no framework, no build step. Same approach as idezign-site: hand-written, fast, minimalist.

- **Hosting:** Cloudflare Pages (auto-deploys on push to `main`, ~2 min lag)
- **Domain:** idezign.com (Cloudflare DNS, CNAME @ → idezign-com.pages.dev)
- **Fonts:** Jost (Google Fonts), weights 200/300/400/500
- **Brand:** red `#A82828` on black `#0c0c0c` — the dark twin of idezign.ai's white scheme

## Layout

```
idezign-com/
├── index.html        # homepage (dark)
├── ai/index.html     # animated transition page → idezign.ai ("the intelligence side of things")
└── logos/            # wordmarks, favicons, og images
```

## Cross-site wiring

- This site's band + footer link to `/ai/` — an animated landing page (neural network assembling) that continues to **idezign.ai**
- idezign.ai links to `/com/` over there — the mirror page (network build-out animation) that continues back to **idezign.com**

## Deploy flow

1. Edit on `main` (GitHub web UI, local clone, or via Cowork + Chrome extension)
2. Push / commit
3. Cloudflare Pages builds automatically
4. Live at idezign.com in ~2 minutes

No manual publish step. Push = live.
