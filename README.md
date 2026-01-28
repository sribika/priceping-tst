# PricePing

Competitor price and stock alerts for small sellers.

PricePing monitors competitor listings and notifies you when prices, stock, or promos change — so you can react fast instead of checking listings all day.

---

## Why PricePing

In competitive marketplaces, small changes matter:
- A competitor drops price
- A top seller goes out of stock
- A promo badge appears
- Shipping cost changes

Most sellers notice too late — after margin or rank is already hit.

PricePing gives you timely alerts so you can respond within hours, not days.

---

## Who It’s For

- Amazon sellers
- Shopify store owners
- Small brand operators
- Marketplace sellers managing competitive SKUs

Typical users:
- Monitor dozens (not thousands) of competitors
- Make pricing decisions themselves
- Already pay for seller tools
- Work on PC/laptop daily

---

## Core Problem

Today, sellers:
- Manually check competitor listings
- Miss changes while busy or offline
- React too late to price drops or stock-outs

This costs:
- Margin
- Buy Box position
- Time and focus

PricePing automates competitor monitoring and turns changes into clear alerts.

---

## Core Workflow

### 1. Add Competitors (Input)
- Paste competitor URLs or SKUs
- Choose what to track:
  - Price
  - Shipping cost
  - Stock status
  - Promo badge (deal, coupon)

No catalog sync required.

---

### 2. Scheduled Checks (Process)
- Listings are checked on a schedule (2–6x per day)
- Changes are detected and logged
- History is stored based on plan limits

Checks are rate-limited to stay reliable and cost-safe.

---

### 3. Alerts & Weekly Summary (Output)
You receive:
- Instant alerts (email / Slack):
  - “Competitor A dropped price from $29 → $25”
  - “Competitor B is out of stock”
- Weekly “moves” summary:
  - What changed
  - When it changed
  - Simple suggested action

This turns raw changes into decisions.

---

## MVP Features

### Monitoring
- URL/SKU-based tracking
- Price, stock, shipping, promo detection
- Scheduled checks with caps

### Alerts
- Email notifications
- Slack notifications (optional)
- Change-type filters

### History
- Change log per URL
- Limited history window by plan

---

## Pricing Model (LTD-Safe)

### Starter — $59 LTD
- 50 tracked URLs
- 2 checks / day
- 1 seat
- 30-day history

### Growth — $149 LTD
- 200 tracked URLs
- 4 checks / day
- 5 seats
- 180-day history

### Pro — $299 LTD
- 500 tracked URLs
- 6 checks / day
- 10 seats
- 365-day history
- Limited API export

> No unlimited URLs or checks to keep scraping and proxy costs predictable.

---

## Important Safety Notes

- Scraping is resource-intensive and can trigger blocks
- Usage is capped by URLs and checks/day
- Aggressive scraping or unlimited plans are intentionally avoided
- Reliability > frequency

---

## Tech Stack (Suggested)

- **Frontend:** Next.js
- **Backend:** Laravel
- **Database:** PostgreSQL / MySQL
- **Scheduler:** Cron / Laravel Scheduler
- **Notifications:** Email, Slack webhooks
- **Scraping:** Headless browser + proxy rotation (rate-limited)

---

## Suggested Repo Structure

```

priceping/
├─ backend/        # Laravel API + schedulers
├─ web/            # Next.js dashboard
└─ README.md

````

---

## Local Development

### Backend (Laravel)

```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan schedule:work
php artisan serve
````

### Frontend (Next.js)

```bash
cd web
npm install
npm run dev
```

Create `.env.local`:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000/api
```

---

## Competitors & Positioning

* **Prisync** — enterprise-focused, product-based pricing
* **Price2Spy** — complex, higher learning curve
* **Keepa** — Amazon-only
* **camelcamelcamel** — free, limited workflows

PricePing focuses on:

> **Small sellers, fewer URLs, faster setup, actionable alerts.**

---

## Roadmap

### v1 (Validation)

* URL monitoring
* Price/stock alerts
* Weekly summary
* History caps

### v1.5

* Promo badge detection
* Team roles
* Webhook delivery

### v2

* Marketplace-specific rules
* Suggested pricing actions
* Advanced filters and grouping

---

## License

TBD (MIT or proprietary SaaS license)
