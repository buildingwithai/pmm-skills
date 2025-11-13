# AI Product Pricing Strategies

Price AI/ML products for value capture and sustainable unit economics.

## Overview

**AI pricing challenge:** Cost structure differs from traditional SaaS

**Traditional SaaS:** Fixed infrastructure cost (scales cheaply)
**AI products:** Variable compute cost (GPT-4 API, training, inference)

**2024 trends:**
- 67% of AI products use usage-based or hybrid pricing
- Avg gross margin: 60-75% (vs 80-90% traditional SaaS)
- Avg cost per inference: $0.001-$0.10 (depending on model)

**Key question:** How to price when costs are variable and high?

## AI Cost Structure

### Inference Costs

**Cost drivers:**
- Model size (GPT-4: $0.03/1K tokens, GPT-3.5: $0.0015/1K tokens)
- Inference frequency (how often users query)
- Input/output length (more tokens = higher cost)

**Example: ChatGPT Plus**
- Cost per GPT-4 query: ~$0.02-$0.05 (estimated)
- User queries: 50-100/day (heavy user)
- Monthly cost: $30-150 (variable)
- Price: $20/month (flat)
- **Challenge:** Power users unprofitable (150 queries/day × $0.03 = $135 cost vs $20 revenue)

---

### Training/Fine-Tuning Costs

**One-time or periodic:**
- Initial training: $10K-$1M (depending on model size, data)
- Fine-tuning: $1K-$50K per iteration
- Ongoing retraining: Monthly/quarterly

**Amortization:** Spread cost across customers

**Example:**
- Fine-tune model: $10K
- 1,000 customers
- Cost per customer: $10 (one-time)

---

### Data Costs

**Acquisition, storage, processing:**
- Data licensing (if using proprietary data)
- Storage (vector databases, embeddings)
- Processing (ETL, cleaning, labeling)

**Varies:** Depends on data volume and complexity

---

## AI Pricing Models

### Model 1: Usage-Based (Consumption)

**Charge per API call, token, inference, prediction**

**Example: OpenAI API**
- GPT-4: $0.03/1K input tokens, $0.06/1K output tokens
- GPT-3.5: $0.0015/1K input tokens, $0.002/1K output tokens
- Whisper (audio): $0.006/minute

**Pros:**
- ✅ Aligns cost with revenue (pay what you use)
- ✅ Low barrier to entry ($0 start, pay as you scale)
- ✅ Fair (power users pay more)

**Cons:**
- ❌ Unpredictable revenue (usage fluctuates)
- ❌ Customer anxiety ("How much will I pay?")
- ❌ Complex billing (metering, aggregation)

**Best for:** API/platform products (developers, enterprises integrating AI)

---

### Model 2: Hybrid (Subscription + Usage)

**Base subscription + usage overage**

**Example: Jasper AI (AI writing)**
- Base: $49/month (includes 50K words)
- Overage: $0.001/word beyond 50K

**Example: Midjourney (AI image generation)**
- Basic: $10/month (~200 images)
- Standard: $30/month (~900 images)
- Pro: $60/month (unlimited, but throttled after ~15K)

**Pros:**
- ✅ Predictable base revenue (subscription)
- ✅ Expansion upside (usage)
- ✅ Reduces customer anxiety (know minimum cost)

**Cons:**
- ⚠️ Complexity (subscription + usage tracking)
- ⚠️ Still have margin risk (power users)

**Best for:** End-user AI products (writing, design, analysis)

---

### Model 3: Flat Subscription (Unlimited*)

**Fixed price, "unlimited" usage (with soft caps)**

**Example: ChatGPT Plus**
- $20/month (unlimited GPT-4, but rate-limited to ~40 messages/3 hours)

**Example: Grammarly Premium**
- $12/month (unlimited AI writing suggestions)

**Pros:**
- ✅ Simple (customers love "unlimited")
- ✅ Predictable revenue (MRR stable)
- ✅ Low customer anxiety

**Cons:**
- ❌ Margin risk (power users unprofitable)
- ❌ Requires throttling/rate limits (to control costs)

**Best for:** Consumer products (B2C), high volume

---

### Model 4: Tiered Subscription (Usage Buckets)

**Tiers with different usage caps**

**Example: Copy.ai (AI copywriting)**
- Free: 2,000 words/month
- Pro: $49/month (unlimited words, 5 users)
- Enterprise: Custom (unlimited words, unlimited users)

**Example: Synthesia (AI video)**
- Personal: $30/month (10 minutes video/month)
- Corporate: $90/month (30 minutes video/month)
- Enterprise: Custom (unlimited)

**Pros:**
- ✅ Familiar (Good/Better/Best)
- ✅ Predictable revenue
- ✅ Manages costs (caps usage)

**Cons:**
- ⚠️ Customers hit caps (frustration)
- ⚠️ Hard to price (what's the right cap?)

**Best for:** SMB/mid-market AI products

---

### Model 5: Seat-Based (Ignoring Usage)

**Charge per user, unlimited usage**

**Example: Notion AI**
- $10/user/month (unlimited AI queries per user)

**Example: GitHub Copilot**
- $10/user/month (unlimited code suggestions)

**Pros:**
- ✅ Simple (familiar SaaS pricing)
- ✅ Predictable revenue
- ✅ No usage tracking needed

**Cons:**
- ❌ Margin risk (power users expensive)
- ❌ Doesn't align with value (usage varies 10x between users)

**Best for:** B2B products where seat-based is norm (developer tools, productivity)

---

## Pricing AI Features (Add-On to Existing Product)

### Add-On Pricing

**Scenario:** Existing SaaS product adding AI features

**Option 1: Flat add-on**
- Base product: $49/month
- AI add-on: +$20/month (unlimited AI features)

**Example: Notion AI**
- Notion base: $10/user/month
- Notion AI: +$10/user/month

---

**Option 2: Usage-based add-on**
- Base product: $49/month
- AI credits: $0.10 per AI query (buy in packs of 100 = $10)

**Example: Canva**
- Canva Pro: $13/month
- AI image generation: 100 credits/month included, $0.10/credit for more

---

**Option 3: Tiered add-on**
- Base product: $49/month
- AI Basic: +$10/month (100 AI queries)
- AI Pro: +$30/month (unlimited AI queries)

---

### Bundling vs Unbundling

**Bundle (include AI in all tiers):**
- Pros: Easier to sell (one price), everyone gets AI
- Cons: Power users unprofitable, can't monetize separately

**Unbundle (AI as separate SKU):**
- Pros: Monetize AI separately, manage costs, upsell opportunity
- Cons: More complex (two bills), some customers won't buy

**Recommendation:** Start bundled (test adoption), unbundle later (if costs high or adoption low)

---

## Controlling AI Costs

### Tactic 1: Rate Limiting

**Throttle usage to manage costs**

**Example: ChatGPT Plus**
- Limit: 40 GPT-4 messages per 3 hours
- If exceeded: Fallback to GPT-3.5 (cheaper)

**Implementation:** 
- Hard limit (stop after 40)
- Soft limit (slow down, deprioritize)

---

### Tactic 2: Model Selection

**Offer multiple models with different costs/capabilities**

**Example: OpenAI API**
- GPT-4: $0.03/1K tokens (expensive, best quality)
- GPT-3.5: $0.0015/1K tokens (cheap, good quality)
- Customer chooses (or auto-route based on task complexity)

**Savings:** 20x cost difference (GPT-4 vs GPT-3.5)

---

### Tactic 3: Caching & Optimization

**Reduce redundant API calls**

**Tactics:**
- Cache common queries (FAQ, repeated prompts)
- Batch requests (multiple queries in one API call)
- Prompt optimization (shorter prompts = fewer tokens)

**Savings:** 20-40% cost reduction

---

### Tactic 4: Tiered Features (Gating)

**Gating expensive AI features to higher tiers**

**Example: Jasper AI**
- Starter: Basic AI writing (GPT-3.5 equivalent)
- Pro: Advanced AI (GPT-4 equivalent) + brand voice + SEO

**Reasoning:** Power users (who need GPT-4) pay more, subsidize basic users

---

### Tactic 5: Committed Use Discounts

**Incentivize predictable usage**

**Example: OpenAI API**
- Pay-as-you-go: $0.03/1K tokens
- Commit to $1K/month: $0.025/1K tokens (17% discount)
- Commit to $10K/month: $0.020/1K tokens (33% discount)

**Benefit:** Predictable revenue (for you) + discount (for customer)

---

## AI Value Metrics

### Metric 1: Per-Inference/Query

**Charge per API call, prediction, generation**

**Examples:**
- OpenAI: Per token
- Hugging Face: Per API call
- Anthropic: Per token

**When to use:** API/platform products, developers

---

### Metric 2: Per-Outcome

**Charge per result/output (not input)**

**Examples:**
- $0.50 per AI-generated article
- $1 per AI-generated image
- $5 per AI-analyzed document

**When to use:** Outcome is clear and valuable (easier for customer to understand value)

---

### Metric 3: Per-Seat

**Charge per user with access to AI features**

**Examples:**
- Notion AI: $10/user/month
- GitHub Copilot: $10/user/month

**When to use:** B2B, team products, familiar model

---

### Metric 4: Per-Data-Volume

**Charge per GB of data processed**

**Examples:**
- $0.10/GB for AI data processing
- $1/1K records analyzed

**When to use:** Data-heavy AI (classification, ETL, labeling)

---

## Pricing Psychology for AI

### Anchoring to Value (Not Cost)

**Bad:** "We charge $0.05/query because it costs us $0.03"
**Good:** "We charge $0.50/query because it saves you 30 minutes of work ($25 value)"

**Value-based pricing:**
- AI writing: Saves 2 hours/week → $100 value/week → $50/month pricing justified
- AI design: Replaces $50/hour designer → $500 value/month → $100/month pricing

**Formula:** Price = 10-20% of value delivered (capture fraction, leave customer with 80-90% value)

---

### "Unlimited" Perception (With Hidden Caps)

**Messaging:** "Unlimited AI writing" (sounds great)
**Reality:** Rate-limited to 1,000 queries/day (covers 99% of users)

**Why it works:** Customers love "unlimited" (removes anxiety), caps prevent abuse

**Caveat:** Don't hide caps (disclose in FAQ/terms), or backlash

---

### Free Tier for AI

**Challenge:** AI costs $ per query (unlike traditional SaaS)

**Options:**

**Option 1: Generous trial (time-limited)**
- 14-day trial, unlimited usage
- After trial: Pay or lose access

**Option 2: Credit-based free tier**
- Free: 100 AI queries/month
- Paid: 1,000+ queries/month

**Option 3: Freemium with AI teaser**
- Free: 10 AI queries/month (enough to experience value)
- Paid: Unlimited

**Recommendation:** Option 3 (credit-based freemium) balances access + cost control

---

## Case Studies

### OpenAI (API Usage-Based)

**Model:** Per-token pricing (GPT-4, GPT-3.5, DALL-E, Whisper)

**Pricing:**
- GPT-4: $0.03/1K input tokens, $0.06/1K output
- GPT-3.5: $0.0015/1K input, $0.002/1K output

**Results:**
- $3.4B ARR (2024 estimated)
- Developers love usage-based (pay what you use)
- High margin customers (enterprises with committed use)

**Why it works:** Developer audience (comfortable with usage-based), clear cost-to-revenue mapping

---

### ChatGPT Plus (Flat Subscription)

**Model:** $20/month unlimited (rate-limited)

**Pricing:**
- Free: GPT-3.5, limited usage
- Plus: $20/month, GPT-4, unlimited (40 messages/3 hours cap)

**Results:**
- 10M+ subscribers (2024 estimated)
- $200M+/month revenue

**Challenges:**
- Power users unprofitable (some users cost $50-100/month)
- Rate limits frustrate heavy users

**Why it works:** Consumer product (simple, predictable), huge volume (subsidizes power users)

---

### Jasper AI (Hybrid Subscription + Usage)

**Model:** Subscription (includes words) + overage

**Pricing:**
- Creator: $49/month (50K words)
- Teams: $125/month (unlimited words, 3 users)
- Business: Custom

**Results:**
- $125M ARR (2023 estimated)
- 100K+ customers

**Why it works:** Predictable for customers (base price), expansion revenue (overages), manages costs (caps)

---

## Key Takeaways

1. **67% of AI products use usage-based or hybrid** (2024)
2. **AI margins: 60-75%** (vs 80-90% traditional SaaS) - Manage costs carefully
3. **Hybrid = best of both worlds** - Subscription (predictable) + usage (expansion)
4. **Rate limiting essential** - Control costs (ChatGPT: 40 messages/3 hours)
5. **Price on value, not cost** - AI writing saves $100/week → charge $50/month
6. **Free tier: 10-100 credits** - Balance access + cost control
7. **Committed use discounts** - Incentivize predictable usage (17-33% discount)

## Next Steps

**Design usage-based pricing:**
→ Read `advanced/usage-based-pricing-deep-dive.md`

**Select value metric:**
→ Read `core/05-selecting-value-metrics.md`

**Control costs with tiering:**
→ Read `core/06-packaging-tier-design.md`
