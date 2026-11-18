# ThingsBoard Cloud vs. 8 GB Linux VPS Cost Calculator (2026)

Standalone, zero-dependency interactive TCO calculator comparing **ThingsBoard Cloud** (including Traffic Packs, Storage Packs, and raw TTL retention) against **ThingsBoard 4.4 Self-Hosted** under the BUSL 1.1 Free License (≤100 devices, 1 production server) on an **8 GB KVM VPS (RackNerd)**.

## Default Example (20 ESP32s × 5 metrics every 10s) 

- **Transport messages / month:** `5,184,000`
- **Data points / month:** `25,920,000`
- **Cloud Free ($0, 1M pts):** Exhausted in **~28 hours**
- **Cloud Prototype ($49/mo base, 10M pts):** Needs **4 Traffic Packs ($5 each) = $69/mo** (30-day TTL) or **$79/mo** (60-day default TTL with 1 Storage Pack)
- **Cloud Pilot ($149/mo):** Needed if Traffic Packs aren't used or when scaling above 50 devices
- **Self-Hosted 8 GB KVM VPS (RackNerd):**
  - Annual KVM special: **~$119.99/yr (~$10.00/mo)** locked recurring
  - Standard monthly KVM: **$36.59/mo** (6 vCPU, 220 GB SSD, no annual lock-in)
- **PostgreSQL storage rule of thumb:** `~14 MB × points/sec × days` → `~25 GB` for 180 days, `~51 GB` for 365 days

## Deploy to GitHub Pages (60 seconds)

1. Push `index.html`, `pricing-data.json`, `README.md`, and `LICENSE` to a public GitHub repository (e.g., `thingsboard-tco-calculator`).
2. Go to **Settings → Pages → Deploy from a branch (`main` / `root`)**.
3. Copy your live `https://<username>.github.io/<repo>/` URL into your `dev.to` article.
4. Once the `dev.to` article is live, set `const articleUrl = "..."` in `index.html` and commit.

## Sources (Verified Nov 2026)
- [ThingsBoard Cloud Pricing](https://thingsboard.io/pricing/)
- [ThingsBoard Subscriptions, Quotas & Top-Ups](https://thingsboard.io/docs/paas/reference/subscriptions/)
- [ThingsBoard 4.4 BUSL 1.1 License](https://github.com/thingsboard/thingsboard#license)
- [ThingsBoard Docker Sizing](https://thingsboard.io/docs/installation/docker/)
- [RackNerd KVM VPS Plans](https://www.racknerd.com/kvm-vps)

*Disclosure: The calculator includes clearly labeled affiliate links below the comparison results.*
