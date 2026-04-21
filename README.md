# AutoCon 5 — Program Guide

Static website for the AutoCon 5 conference program guide.

## Structure

```
autocon5-site/
├── index.html       # All content — edit talks, sponsors, copy here
├── style.css        # All styles — fonts, colors, layout here
└── logos/           # All image assets
    ├── ac5.png              # AutoCon 5 logo (no tagline)
    ├── ac5-tagline.png      # AutoCon 5 logo with tagline (used in hero)
    ├── naf.png              # NAF logo (used in nav)
    ├── naf-tag.png          # NAF logo with tagline (used in footer)
    ├── netbrain.png         # Accelerating sponsor
    ├── cisco.svg            # Sustaining
    ├── itential.png         # Sustaining
    ├── netboxlabs.png       # Sustaining
    ├── arista.png           # Supporting
    ├── codaxy.png           # Supporting
    ├── flock9.png           # Supporting
    ├── forwardnetworks.png  # Supporting
    ├── ipfabric.png         # Supporting
    ├── kentik.png           # Supporting
    ├── ntc.png              # Supporting
    ├── opentext.png         # Supporting
    ├── opsmill.png          # Supporting
    ├── flexoptix.png        # Friends of NAF
    ├── netcraft.png         # Friends of NAF
    ├── packetpushers.png    # Official Media Partner
    └── packetcoders.png     # Official Training Partner
```

## Brand

- **Fonts:** Rama Gothic E (display/headings) · Space Mono (body/UI) — loaded from Google Fonts
- **Colors:** `#000000` black · `#FFFFFF` white · `#FFFF00` yellow · `#DCDCDC` gray

## Sponsor logo sizes (CSS in style.css)

Logo containers use `object-fit: contain` so logos fill their box proportionally regardless of source dimensions. To adjust sizes, edit the `.tier-*` rules in `style.css`:

| Tier | Container size                |
|------|-------------------------------|
| Accelerating (NetBrain) | 260×90px                      |
| Sustaining | 160×60px                      |
| Supporting | 120×40px                      |
| Friends of NAF | 96×42px                       |
| Partners | 160×60px (matches Sustaining) |

## Deploy to Cloudflare Pages

1. Push this folder to a GitHub repo
2. In Cloudflare Pages, connect the repo
3. Build command: *(none — plain static site)*
4. Output directory: `/` (or the folder name if nested)

No build step required. Cloudflare Pages will serve `index.html` directly.

## Known items

- Flexoptix logo is white-on-transparent — renders correctly on the dark background
- Cisco logo is SVG (smaller file, scales perfectly)
- Packet Pushers logo is the colored version (white mono not available in current assets)
