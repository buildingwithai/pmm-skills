# Pricing Page Design

Design pricing pages that convert visitors into customers.

## Overview

Your pricing page is often the highest-intent page on your website. Visitors here are ready to buy—don't lose them with poor design.

**Impact:** Well-designed pricing pages convert 10-25% better than poorly designed ones (2024 CRO data).

**Elena Verna's DNA of Great Pricing Page (2024):**
1. **Clarity** - Understand options in 10 seconds
2. **Comparison** - Easy to compare tiers
3. **Conversion** - Clear path to purchase

## Essential Elements

### 1. Value Proposition (Above the Fold)

**What it is:** One sentence explaining what you do and why it matters.

**Bad:** "Our pricing" (no context)
**Good:** "Choose the plan that fits your team. Trusted by 10,000+ companies."

**Elements:**
- Product category (what you are)
- Key benefit (why it matters)
- Social proof (who uses you)

**Example: Notion**
```
"One workspace. Every team."
Collaborative workspace for notes, docs, wikis, and projects.
Trusted by teams at Apple, Pixar, and NASA.
```

---

### 2. Billing Toggle (Monthly/Annual)

**Best practice:** Toggle between monthly and annual pricing.

**Default:** Show monthly (lower sticker shock), highlight annual savings.

**Visual:**
```
○ Monthly    ● Annual (Save 20%)
```

**Annual savings display:**
- "Save $240/year" (dollar amount)
- "2 months free" (alternative framing)
- Both (belt-and-suspenders)

---

### 3. Tier Cards (3-4 Tiers)

**Layout:** Horizontal cards, left-to-right or centered.

**Highlighted tier:**
- Visual distinction (color, border, elevation)
- Badge ("Most Popular", "Best Value")
- Slightly larger card

**Per-tier content:**
- **Tier name** (Professional, Business, Enterprise)
- **Price** (large, prominent)
- **Billing cadence** ("/month", "/year", "/user/month")
- **Tagline** (1 sentence: who this is for)
- **Key features** (5-8 bullet points)
- **CTA button** ("Get Started", "Start Free Trial", "Contact Sales")

**Example card:**
```
PROFESSIONAL (Most Popular badge)
$149/month
Billed annually ($1,788/year)

For growing teams

✓ Unlimited projects
✓ Advanced analytics
✓ Priority support
✓ 100 GB storage
✓ API access

[Get Started →] (prominent button)
```

---

### 4. Feature Comparison Table

**When to include:** Below tier cards, for detailed comparison.

**Best practices:**
- **5-10 features max** (not 30)
- **Group by category** (Core, Advanced, Support, Security)
- **Check marks** (✓) for included, not text
- **Expandable sections** for less important features (progressive disclosure)

**Example:**
```
Feature             | Starter | Pro    | Business
--------------------|---------|--------|----------
Users               | 5       | 25     | Unlimited
Projects            | 10      | ∞      | ∞
Analytics           | Basic   | Adv.   | Custom
Support             | Email   | Priority| Phone+CSM
SSO/SAML            | ✗       | ✗      | ✓
```

**Mobile:** Stack vertically or horizontal scroll (not shrink).

---

### 5. FAQ Section

**Purpose:** Address objections before they become barriers.

**Common questions:**
- "Can I change plans later?" (Yes, anytime)
- "What payment methods do you accept?" (Credit card, ACH, invoice for annual)
- "Is there a free trial?" (Yes, 14 days, no credit card required)
- "Can I cancel anytime?" (Yes, no long-term contracts)
- "What's included in support?" (Email for all, phone for Business+)
- "Do you offer discounts?" (Yes, 20% for annual, non-profit, education)
- "Is my data secure?" (Yes, SOC 2, encryption, etc.)
- "What happens if I exceed my plan limits?" (Prompts to upgrade, or usage overage fees)

**Best practice:** 5-8 FAQs, concise answers.

---

### 6. Social Proof

**Types:**
- **Customer logos:** "Trusted by [Apple, Microsoft, Netflix]"
- **Reviews:** "4.8/5 stars from 2,000 reviews on G2"
- **User count:** "Join 50,000+ teams"
- **Case studies:** "See how [Company] increased revenue 40% with [Product]"

**Placement:** 
- Above tier cards (builds trust before price)
- Below tier cards (reinforces decision)
- Both (max credibility)

---

### 7. Clear CTAs (Call-to-Action)

**CTA copy variants:**
- "Start Free Trial" (for freemium/trial)
- "Get Started" (generic, works for most)
- "Buy Now" (direct, transactional)
- "Contact Sales" (enterprise)
- "Try Free for 14 Days" (specific, reduces risk)

**Color:** Contrasting, stands out (often blue, green, orange vs neutral page)

**Micro-copy under CTA:**
- "No credit card required"
- "Cancel anytime"
- "14-day money-back guarantee"

---

### 8. Add-Ons (Optional)

**When to show:** If you have à la carte options.

**Placement:** Below main tiers or separate section.

**Example:**
```
Add-Ons (Optional)
- Advanced analytics: +$50/month
- Dedicated CSM: +$500/month
- Custom integrations: Contact us
```

**Don't overdo:** >5 add-ons = overwhelming.

---

## Layout Best Practices

### Above the Fold (First Screen)

**Must include:**
- Value proposition
- Monthly/Annual toggle
- At least top 2 tiers visible (if 3-4 tier structure)

**Don't bury:** Users should see pricing within 2 seconds of landing.

---

### Mobile Responsiveness

**40%+ of traffic is mobile** (2024 data).

**Mobile-specific designs:**
- Stack tiers vertically (not horizontal squish)
- Sticky CTA button at bottom
- Simplified comparison table (horizontal scroll or just key features)
- Collapsible FAQ

**Test on mobile:** Most B2B buyers research on mobile, buy on desktop.

---

### Page Load Speed

**Target:** <2 seconds load time

**Why:** Each 1-second delay = 7% conversion loss

**Optimization:**
- Lazy load images
- Minimize JavaScript
- CDN for static assets
- Compress images

---

## Pricing Page Variations

### Variation 1: Simple (2-Tier, SMB)

**Layout:**
```
Free             Pro
$0/month         $49/month

[Basic]          [Full features]
[Try Free]       [Start Trial]
```

**When to use:** Simple product, limited tiers, SMB focus

---

### Variation 2: Standard (3-Tier + Enterprise)

**Layout:**
```
Starter          Professional     Business        Enterprise
$49/month        $149/month       $399/month      Contact Sales
(Most Popular highlighted)
```

**When to use:** Most common, serves SMB → Enterprise

---

### Variation 3: Freemium + Paid Tiers

**Layout:**
```
Free              Plus            Business        Enterprise
$0 forever        $10/user/mo     $20/user/mo     Custom

[Get Started]     [Start Trial]   [Start Trial]   [Contact Sales]
```

**When to use:** PLG motion, viral products

---

### Variation 4: Usage-Based Calculator

**Layout:**
```
[Slider: API calls per month]
0 ←―――○―――→ 10M calls

Estimated cost: $247/month

[Breakdown:]
- Base: $99/month
- Usage (5.2M calls × $0.02): $104
- Overage (200K × $0.05): $10
- Tier discount (20%): -$43
Total: $247/month

[Get Started]
```

**When to use:** Usage-based pricing, help customers estimate costs

---

## Copy & Messaging

### Tier Descriptions

**Not:** "Our most popular plan"
**Better:** "For growing teams that need collaboration"

**Formula:** "For [audience] that need [key benefit]"

**Examples:**
- Starter: "For individuals getting started"
- Pro: "For teams collaborating on projects"
- Business: "For companies with advanced needs"
- Enterprise: "For large organizations requiring custom solutions"

---

### Feature Benefits (Not Just Features)

**Not:** "API access" (what)
**Better:** "API access to integrate with your existing tools" (why it matters)

**Not:** "99.99% uptime SLA" (technical)
**Better:** "Your team can rely on always being online" (benefit)

**Formula:** [Feature] + "so you can [benefit]"

---

### Urgency (Ethical)

**Good urgency:**
- "Limited time: 20% off annual plans through Dec 31"
- "Early adopter pricing ends when we hit 1,000 customers"

**Bad urgency:**
- "Only 3 spots left!" (fake)
- "Sale ends tonight!" (permanent)

**Use sparingly:** Overuse trains customers to ignore.

---

## Common Mistakes

### Mistake 1: Hidden Pricing

**Problem:** "Contact us for pricing" on all tiers

**Impact:** 73% of SMB buyers won't engage (2024 Paddle)

**Fix:** Show pricing for SMB/mid-market, "Contact sales" for enterprise only

---

### Mistake 2: Too Many Tiers

**Problem:** 6 tiers, customers paralyzed

**Impact:** Decision paralysis, abandon page

**Fix:** 3-4 tiers maximum

---

### Mistake 3: Feature Overload

**Problem:** 30-feature comparison table

**Impact:** Overwhelming, can't process

**Fix:** Highlight 5-8 key features, expandable "See all features" for rest

---

### Mistake 4: Unclear What's Included

**Problem:** "Pro plan: $99/month" (what do you get?)

**Impact:** Uncertainty, won't commit

**Fix:** List 5-8 key features per tier

---

### Mistake 5: No Social Proof

**Problem:** Just pricing, no credibility signals

**Impact:** Trust concerns, hesitation

**Fix:** Add customer logos, reviews, user count

---

### Mistake 6: Weak CTAs

**Problem:** "Submit" (generic, unclear)

**Impact:** Confusion, low clicks

**Fix:** "Start Free Trial", "Get Started", "Contact Sales" (specific action)

---

### Mistake 7: Not Mobile-Optimized

**Problem:** Horizontal scroll on mobile, tiny text

**Impact:** 40% of traffic can't use page

**Fix:** Responsive design, stack vertically on mobile

---

## A/B Testing Pricing Pages

**What to test:**
- CTA copy ("Get Started" vs "Start Free Trial" vs "Try Free")
- Tier order (high-to-low vs low-to-high)
- Highlighted tier (which gets "Most Popular" badge)
- Feature display (bullets vs icons vs table)
- Social proof placement (above vs below tiers)
- Annual toggle default (monthly vs annual)

**Tools:**
- VWO (Visual Website Optimizer)
- Optimizely
- Google Optimize (free, basic)
- Unbounce (landing pages)

**Sample size:** 250-500 visitors per variation, 30-60 days

See `core/09-pricing-experimentation-testing.md`.

---

## Pricing Page Checklist

Use before launching:

- ☐ Value proposition above the fold
- ☐ Monthly/Annual toggle (if applicable)
- ☐ 3-4 tiers clearly differentiated
- ☐ Target tier highlighted visually
- ☐ 5-8 key features per tier
- ☐ Feature comparison table (expandable for details)
- ☐ Clear CTAs on every tier
- ☐ Social proof (logos, reviews, or user count)
- ☐ FAQ section (5-8 questions)
- ☐ Mobile-responsive (test on phone)
- ☐ Page loads <2 seconds
- ☐ No hidden fees or surprises
- ☐ Consistent with brand (colors, fonts, tone)

---

## Key Takeaways

1. **Elena Verna's DNA: Clarity, Comparison, Conversion**
2. **73% of SMB won't engage without public pricing** - Show prices
3. **Mobile = 40% of traffic** - Must be responsive
4. **5-8 features per tier** - Not 30
5. **Highlight target tier** - Visual distinction + badge
6. **Social proof builds trust** - Logos, reviews, user count
7. **Test everything** - CTA copy, layout, highlighted tier

## Next Steps

**Ready to launch pricing:**
→ Read `core/09-pricing-experimentation-testing.md`

**Need pricing psychology first:**
→ Read `core/07-pricing-psychology-tactics.md`

**Ready to communicate internally:**
→ Read `core/10-internal-alignment-communication.md`
