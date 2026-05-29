# 💰 Online Seller Pricing Calculator

A free, fully client-side pricing calculator built for online sellers — on Shopee, Lazada, TikTok Shop, or any platform. No sign-up, no server, no data sent anywhere. Everything runs in your browser.

> Built specifically with Philippine online sellers in mind, with support for 10 currencies.

---

## ✨ Features

### Core Pricing
- **Cost per unit (COGS)** — enter what you pay or manufacture per item
- **Defect / return rate** — automatically factors waste into your unit cost
- **Additional costs** — add custom per-unit costs (labels, inserts, etc.)
- **Packaging & labor** — per-item overhead tracking

### Platform & Fees
- **Platform fee %** — Shopee, Lazada, TikTok Shop, or any marketplace
- **Affiliate commission %** — TikTok Shop affiliate deductions
- **Tax rate %** — VAT or income tax
- **Platform presets** — one-click fee setup for Shopee, Lazada, TikTok Shop, Wholesale
- **Custom presets** — save your own platform fee configurations

### Ads & Marketing
- **Monthly ad spend** — enter your total monthly ad budget (Facebook, TikTok, Shopee Ads)
- Auto-calculates cost per unit and shows it as a live hint

### Smart KPIs (live, instant)
| KPI | Description |
|---|---|
| Cost per unit | Total cost to sell 1 item |
| Break-even price | Minimum price to avoid a loss |
| Suggested price | 3× cost rule-of-thumb |
| Profit per item | Net after all fees |
| Profit margin | % of selling price |
| Monthly profit | At your target volume |
| Monthly revenue | Gross sales |
| Total ads spend | With % of revenue indicator |

### Profit Goal Calculator
- Set a **monthly profit target** (e.g. ₱50,000/month)
- **Option A** — how many units to sell at the current price
- **Option B** — what price to charge at the current volume
- One-click apply buttons to update the calculator instantly
- Summary bar shows how far you are from your goal

### Sale / Voucher Simulator
- Simulate any discount — **% off** or **fixed amount off**
- Quick picks: 5%, 10%, 15%, 20%, 25%
- Shows sale price, payout, profit per item, margin, monthly profit, profit lost
- Smart status banner:
  - 🔴 Loss — selling below break-even
  - 🟡 Thin margin — profitable but barely
  - ✅ Healthy — safe to run the sale

### Price Comparison Table
- Add multiple price points and compare them side by side
- Columns: Selling price, You receive, Profit/item, Margin, Monthly profit, Status
- Status badges: 🔴 Loss / 🟡 Low / 🔵 OK / 🟢 Great

### Save & Load Products
- Save unlimited product setups to browser localStorage
- Load, update, or delete saved products
- Saved products bar with timestamps

### Export / Import
- **Export to Excel (.xlsx)** — inputs + results + price comparison sheet
- **Import from Excel** — restore a previously exported setup

### Multi-Currency Support
Switch between 10 currencies with one click:
`USD ($)` `EUR (€)` `GBP (£)` `PHP (₱)` `MYR (RM)` `SGD (S$)` `INR (₹)` `CNY (¥)` `AUD (A$)` `CAD (C$)`

### Dark Mode
- Toggle between light and dark with a single button
- Preference saved to localStorage — persists across sessions

### Mobile Responsive
- Works on all screen sizes
- Stacked layout on mobile with no overlapping labels

---

## 🚀 Getting Started

This is a **single HTML file** — zero dependencies to install, zero build steps.

### Run locally
```bash
# Clone the repo
git clone https://github.com/your-username/seller-pricing-calculator.git
cd seller-pricing-calculator

# Open directly in browser
open index.html

# Or serve with any static server
npx serve .
python -m http.server 3000
```

### Deploy to GitHub Pages
1. Push `index.html` to your repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your calculator is live at `https://your-username.github.io/repo-name`

---

## 🧮 How the Calculations Work

```
COGS per item  = Unit cost
Defect waste   = COGS × defect% ÷ (1 − defect%)
Ad cost/unit   = Monthly ad spend ÷ target units
Total cost     = COGS + defect waste + packaging + labor + ad cost + additional costs

Platform fee   = Selling price × platform%
Affiliate fee  = Selling price × affiliate%
Tax            = Selling price × tax%
You receive    = Selling price − platform fee − affiliate fee − tax

Net profit     = You receive − Total cost
Break-even     = Total cost ÷ (1 − platform% − affiliate% − tax%)
Suggested price= Total cost × 3
```

---

## 🗺️ Roadmap

- [ ] Shipping cost per item (J&T, Ninja Van, LBC)
- [ ] Platform comparison view (same product, Shopee vs Lazada vs TikTok side by side)
- [ ] Exchange rate / sourcing cost (USD/CNY → PHP for Alibaba/Taobao sourcing)
- [ ] Capital / inventory investment calculator
- [ ] PDF export
- [ ] PWA / installable on mobile
- [ ] Login + cloud save (Supabase)
- [ ] Subscription billing (PayMongo / GCash)

---

## 🛠️ Tech Stack

| | |
|---|---|
| Language | Vanilla HTML, CSS, JavaScript |
| Export/Import | [SheetJS (xlsx)](https://sheetjs.com/) |
| Fonts | Inter + JetBrains Mono (Google Fonts) |
| Storage | Browser localStorage |
| Hosting | GitHub Pages / Vercel / Netlify |

No frameworks. No build tools. No backend. Just one file.

---

## 📁 Project Structure

```
seller-pricing-calculator/
└── index.html        # Entire app — HTML + CSS + JS in one file
```

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/shipping-cost`)
3. Commit your changes (`git commit -m 'Add shipping cost field'`)
4. Push to the branch (`git push origin feature/shipping-cost`)
5. Open a Pull Request

---

## 📄 License

[MIT](LICENSE) — free to use, modify, and distribute.

---

<p align="center">Made for online sellers 🛍️ · Calculate costs, fees, profit & break-even — free forever.</p>
