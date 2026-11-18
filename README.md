# SwapMeep

Board game collection tracker for a small group of friends: incoming pledges, owned copies, games for sale or trade, and sales, with BGG sync review, group swap matches, and scores from the reviewers each user follows.

**Status:** clickable prototype. A single static page (`index.html`) with embedded data and no build step.

## What's in the prototype
- **My collection:** Incoming / Owned / For sale / Sold lanes, per physical copy
- **BGG sync review:** proposed BGG status changes, approved before anything is pushed (simulated in the prototype)
- **Needs attention:** unanswered surveys, stale BGG preorder flags, duplicates
- **Group & friend shelves:** matches between one member's trade list and another's wishlist
- **Reviewers I follow:** per-user follow list. Scores come from reviewers' public BGG ratings; review videos link to YouTube
- **Market & Hot:** sample data only

## Data sources (as of 2026-11-17)
- Collections: public BGG collection pages (harrisc, marLONE). Jules and Ren are sample accounts.
- Pledges and sales: Harris's Gmail subject lines (Kickstarter, Gamefound, BackerKit, eBay).
- Reviewer scores: public BGG ratings of TomVasel, ZeeGarcia and rahdo.
- Videos, channel avatars and thumbnails: links to YouTube. Game thumbnails: links to BGG's image CDN. Images are loaded live by the browser, not stored in this repo.
- Prices, market signals and Hot ranks are **sample values**.

## Deploy (Cloudflare Pages)
Workers & Pages → Create → Pages → Connect to Git → `harris-chiu/swapmeep`
- Framework preset: None
- Build command: *(empty)*
- Build output directory: `/`

Every push to `main` redeploys.

**Privacy:** the page contains real collection and purchase data. Put it behind Cloudflare Access (Zero Trust → Access → Applications) so only invited emails can open it.
