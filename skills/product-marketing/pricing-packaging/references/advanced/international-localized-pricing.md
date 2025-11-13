# International & Localized Pricing

Optimize pricing for global markets.

## Overview

**Global pricing challenge:** Same product, different willingness to pay across countries.

**2024 data:**
- US baseline: 100%
- Western Europe: 80-120% of US
- Nordics (DK, NO, SE): +20-30% premium
- Eastern Europe: 40-60% of US
- Southeast Asia: 40-60% of US
- Latin America: 50-70% of US

**Key decision:** Single global price vs localized pricing

## Single Global Price vs Localized

### Single Global Price

**Model:** Same price everywhere ($99/month worldwide)

**Pros:**
- ✅ Simple (one price, one billing system)
- ✅ No arbitrage concerns (can't buy cheap in India, use in US)
- ✅ Fair (same product, same price)

**Cons:**
- ❌ Underpriced in high-WTP markets (leave money on table in Nordics)
- ❌ Overpriced in low-WTP markets (exclude emerging markets)
- ❌ Currency risk (customers pay USD, but earn EUR/INR)

**When to use:**
- Early-stage (small international customer base)
- Technical products (developers, international audience, USD-comfortable)
- High-value products (price is small vs value, e.g., $10K+ ACV)

**Examples:** AWS, Stripe, OpenAI (mostly single global price in USD)

---

### Localized Pricing

**Model:** Different prices by country/region based on local WTP

**Example:**
- US: $99/month
- Denmark: $119/month (DKK 850)
- India: $49/month (INR 4,000)
- Brazil: $69/month (BRL 350)

**Pros:**
- ✅ Maximize revenue (charge more where WTP higher)
- ✅ Increase access (affordable in emerging markets)
- ✅ Local currency (reduces FX friction)

**Cons:**
- ❌ Complex (multiple price points, billing)
- ❌ Arbitrage risk (VPN to India, buy at $49)
- ❌ Fairness perception ("Why do I pay more?")

**When to use:**
- Scale-stage (significant international revenue)
- Consumer/SMB products (price-sensitive, local currency matters)
- B2C (large volume, localization ROI positive)

**Examples:** Spotify ($10.99 US, $1.99 India), Netflix ($15.99 US, $2.50 India), Adobe

---

## Geographic Willingness to Pay (2024 Data)

### High-WTP Markets (Premium Pricing)

**Nordics (Denmark, Norway, Sweden, Finland):**
- WTP: 120-150% of US
- Reasoning: High income, strong purchasing power, enterprise budgets
- **Denmark example:** +151% higher WTP than US (2024 study)

**Switzerland:**
- WTP: 130-150% of US
- Highest purchasing power in Europe

**Australia:**
- WTP: 100-120% of US
- High income, limited local competition

**Strategy:** Charge 10-20% premium vs US pricing

---

### Medium-WTP Markets (Close to US)

**Western Europe (UK, Germany, France, Netherlands):**
- WTP: 80-100% of US
- Comparable purchasing power, but €/$ exchange rate affects perception

**Canada:**
- WTP: 90-100% of US (CAD vs USD)

**Japan:**
- WTP: 90-110% of US
- High purchasing power, but local competition

**Strategy:** Match or slight discount vs US

---

### Lower-WTP Markets (Discounted Pricing)

**Eastern Europe (Poland, Romania, Czech Republic):**
- WTP: 40-60% of US
- Lower purchasing power, strong local alternatives

**Latin America (Brazil, Mexico, Argentina):**
- WTP: 50-70% of US
- Currency instability, price sensitivity

**Southeast Asia (India, Indonesia, Philippines):**
- WTP: 40-60% of US
- Very price-sensitive, large markets (volume opportunity)

**China:**
- WTP: 60-80% of US
- Large market, local competition (Alibaba, Tencent)

**Strategy:** 40-60% discount vs US to access market

---

## Localization Strategies

### Strategy 1: Regional Pricing Tiers

**Model:** 3-4 regional price bands

**Example:**
- **Tier 1 (High):** US, Canada, Nordics, Switzerland, Australia → $99/month
- **Tier 2 (Medium):** Western Europe, Japan, South Korea → $79/month
- **Tier 3 (Low):** Eastern Europe, Latin America, Southeast Asia → $49/month
- **Tier 4 (Very Low):** India, Nigeria, emerging markets → $29/month

**Implementation:**
- Detect country by IP or billing address
- Show localized price on pricing page
- Charge in local currency (USD, EUR, INR, etc.)

---

### Strategy 2: Purchasing Power Parity (PPP)

**Model:** Price adjusts based on PPP index (World Bank data)

**Formula:** Local Price = US Price × (Local PPP / US PPP)

**Example:**
- US price: $99
- India PPP: 0.42 (42% of US purchasing power)
- India price: $99 × 0.42 = $42

**Tools:**
- **PPP API:** Use World Bank PPP data
- **Automated:** Chargebee, Paddle (built-in PPP)

**Pros:**
- Fair (adjusts for purchasing power)
- Data-driven (World Bank data)

**Cons:**
- Still feels arbitrary to customers
- Arbitrage risk (VPN)

---

### Strategy 3: Currency-Only Localization

**Model:** Same price, different currency

**Example:**
- US: $99
- Eurozone: €99 (not $99 converted to €, but €99)
- UK: £99

**Reasoning:**
- Psychological (€99 "feels" local vs €92.17)
- Simplicity (round numbers)

**Caveat:** May be +/- 10-20% vs true FX rate

---

## Currency & Payment Methods

### Local Currency

**Why it matters:**
- 23% higher conversion when pricing in local currency (2024 Stripe)
- Removes FX confusion ("What is $99 in INR today?")
- Avoids FX fees (bank charges 2-3% for USD transaction)

**How:**
- Use Stripe (supports 135+ currencies)
- Paddle (multi-currency billing)
- Chargebee (global billing)

**Currencies to support:**
- USD (US, international default)
- EUR (Eurozone)
- GBP (UK)
- CAD (Canada)
- AUD (Australia)
- INR (India)
- BRL (Brazil)
- JPY (Japan)

---

### Local Payment Methods

**Beyond credit cards:**

**Europe:**
- SEPA Direct Debit (bank transfer, common for B2B)
- iDEAL (Netherlands)
- SOFORT (Germany)

**Asia:**
- Alipay (China)
- WeChat Pay (China)
- Paytm (India)
- GrabPay (Singapore)

**Latin America:**
- Boleto (Brazil, cash payment at bank)
- OXXO (Mexico, cash at convenience store)

**Why it matters:**
- Credit card penetration low in emerging markets (India 3%, Brazil 20%)
- Local methods increase conversion 30-50%

**Implementation:**
- Stripe (supports 40+ payment methods globally)
- Paddle (optimized for SaaS, multi-currency + local methods)

---

## Preventing Arbitrage

### Problem

**Arbitrage:** Customer in US uses VPN to India, buys at $49 (instead of $99)

**Impact:** Revenue leakage (could be 5-10% of sales)

---

### Solution 1: Billing Address Verification

**Check:** Credit card billing address (not IP)

**Reasoning:** 
- IP can be VPN'd (easy to fake)
- Billing address tied to bank (hard to fake)

**Implementation:**
- Stripe checks billing address automatically
- Decline if mismatch (US user, Indian price)

---

### Solution 2: Geographic Restrictions

**Block:** Certain countries from buying discounted tiers

**Example:**
- India pricing ($49) only available to India billing addresses
- US/EU customers blocked from India pricing

**Con:** Legitimate cases blocked (US expat living in India)

---

### Solution 3: Account Review

**Flag:** Suspicious purchases (VPN, disposable email, mismatch)

**Manual review:** CS team verifies, refunds if abuse

**Effort:** High (requires CS resources)

---

### Solution 4: Accept Some Arbitrage

**Reality:** 1-3% abuse is normal, cost of global pricing

**Trade-off:** Spend engineering time preventing vs accepting loss

**Decision:** If arbitrage <5% revenue, accept it

---

## Tax & Compliance

### VAT (Europe)

**Requirement:** Charge VAT (15-27% depending on country)

**B2C:** Must charge VAT, remit to government
**B2B:** Reverse charge (customer pays VAT, not you)

**Implementation:**
- Stripe Tax (automatic VAT calculation)
- Paddle (Merchant of Record, handles all VAT)
- Quaderno (tax compliance automation)

---

### GST (India, Australia, Canada)

**India GST:** 18% on software (must register if >₹20 lakh revenue)
**Australia GST:** 10% (must register if >$75K AUD revenue)
**Canada GST:** 5-15% (varies by province)

**Implementation:**
- Stripe Tax
- Paddle

---

### US Sales Tax

**Requirement:** Charge sales tax if you have "nexus" (office, employees, $100K+ sales in state)

**SaaS:** Generally exempt in most states (but not all)

**States requiring SaaS tax:** Texas, Pennsylvania, DC, Tennessee, others

**Implementation:**
- Stripe Tax (automatic)
- Avalara (tax compliance platform)

---

## Localization Checklist

Before launching in new country:

- ☐ Research local WTP (surveys, competitors)
- ☐ Determine local pricing (PPP-adjusted or regional tier)
- ☐ Enable local currency (EUR, GBP, INR, etc.)
- ☐ Add local payment methods (SEPA, Alipay, Boleto)
- ☐ Calculate tax obligations (VAT, GST)
- ☐ Implement tax collection (Stripe Tax, Paddle)
- ☐ Update pricing page (auto-detect country, show local price)
- ☐ Translate pricing page (if needed)
- ☐ Set up billing address verification (prevent arbitrage)
- ☐ Test purchase flow (end-to-end in local currency)
- ☐ Communicate to customers (email, blog post)

---

## Case Studies

### Spotify (Localized Pricing)

**Model:** Country-specific pricing based on purchasing power

**Pricing:**
- US: $10.99/month
- India: $1.99/month (82% discount)
- Brazil: $4.99/month (55% discount)
- Norway: $11.99/month (+9% premium)

**Results:**
- 220M+ paid subscribers (2024)
- India: 50M+ users (localized pricing unlocked market)

**Why it works:**
- Consumer product (price-sensitive)
- High volume (TAM = billions)
- Localized pricing = 10x more subscribers in India

---

### Stripe (Global USD Pricing)

**Model:** Same price globally in USD

**Pricing:**
- 2.9% + $0.30 per transaction (worldwide)
- No regional discounts

**Results:**
- $1T+ payment volume (2024)
- 100+ countries

**Why it works:**
- B2B product (less price-sensitive)
- Value-based (% of transaction, scales with customer)
- Developers comfortable with USD

---

### Netflix (Localized Pricing)

**Model:** Country-specific pricing + PPP adjustments

**Pricing:**
- US: $15.99/month (Standard)
- India: $2.50/month (Mobile-only plan)
- Argentina: $3.80/month (Basic)

**Results:**
- 260M+ subscribers (2024)
- Emerging markets = 50%+ of growth

**Why it works:**
- Consumer product (price-sensitive)
- Localized content (Bollywood for India, K-drama for Korea)
- Localized pricing = access to billions of potential subscribers

---

## Key Takeaways

1. **Nordics = +20-30% WTP**, Southeast Asia = -40-60% (vs US baseline)
2. **Local currency = +23% conversion** (Stripe data, 2024)
3. **3-4 regional tiers** - Simplest localization approach
4. **PPP-based pricing** - Fair, data-driven (World Bank)
5. **Billing address verification** - Prevent arbitrage
6. **VAT/GST compliance** - Use Stripe Tax or Paddle
7. **Accept 1-3% arbitrage** - Cost of global pricing

## Next Steps

**Research WTP by country:**
→ Read `core/02-willingness-to-pay-research.md`

**Implement pricing tiers:**
→ Read `core/06-packaging-tier-design.md`

**Launch international pricing:**
→ Read `core/11-launching-new-pricing.md`
