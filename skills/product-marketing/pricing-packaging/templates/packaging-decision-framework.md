# Packaging Decision Framework

Decision tree for feature-to-tier allocation.

## Overview

**Goal:** Decide which features belong in which tier

**Framework:** Value + Adoption + Cost analysis

---

## Feature Evaluation Template

### Feature: [Feature Name]

**Description:**
[1-2 sentences: What does this feature do?]

**Value delivered:**
[What customer problem does it solve? Quantifiable impact?]

---

### Step 1: Value Assessment

**Customer value (1-10):**
- Score: ___/10
- Rationale: ___________

**Value type:**
- [ ] Core value prop (essential to product)
- [ ] Advanced/power user feature
- [ ] Nice-to-have (convenience)
- [ ] Enterprise-specific (security, compliance)

---

### Step 2: Adoption Analysis

**Current adoption (if feature exists):**
- % of users who use this feature: ___%
- Frequency of use: Daily / Weekly / Monthly / Rarely

**Expected adoption (if new feature):**
- [ ] High (80%+ of users will use)
- [ ] Medium (40-80% of users)
- [ ] Low (< 40% of users)
- [ ] Niche (< 10%, specific use case)

---

### Step 3: Cost Analysis

**Cost to deliver:**
- Infrastructure cost: $_____ per customer per month
- Support cost: Low / Medium / High
- Maintenance effort: Low / Medium / High

**Total cost score:**
- [ ] Low cost (<$1 per customer/month)
- [ ] Medium cost ($1-10 per customer/month)
- [ ] High cost (>$10 per customer/month)

---

### Step 4: Competitive Context

**Competitor offering:**
- [ ] All competitors include in basic tier
- [ ] Most competitors include (table stakes)
- [ ] Some competitors include
- [ ] Few/no competitors include (differentiator)
- [ ] We're first to market with this

**Implication:**
- Table stakes → Must include in lower tiers
- Differentiator → Can gate in higher tiers

---

### Step 5: Tier Recommendation

**Decision Matrix:**

| Criteria | Score | Weight | Weighted Score |
|----------|-------|--------|----------------|
| Customer value (1-10) | ___ | 40% | ___ |
| Adoption (High=10, Med=5, Low=2) | ___ | 30% | ___ |
| Cost (Low=10, Med=5, High=2) | ___ | 20% | ___ |
| Competitive (Common=2, Unique=10) | ___ | 10% | ___ |
| **Total** | | | ___ |

**Tier allocation:**
- Score 8-10: Free tier or Tier 1 (core, widely needed)
- Score 5-7: Tier 2 (advanced users)
- Score 3-4: Tier 3 (power users)
- Score 0-2: Enterprise (niche, high-cost, compliance)

**Recommended tier:** ___________

**Rationale:**
___________

---

## Tier Allocation Rules

### Free Tier Rules

**Include if:**
- ✅ Core value prop (can't be free without it)
- ✅ Viral/sharing feature (drives acquisition)
- ✅ Low cost to serve
- ✅ 80%+ adoption

**Exclude if:**
- ❌ High cost (>$1 per user/month)
- ❌ Advanced/power user feature
- ❌ <40% adoption

**Examples:**
- ✓ Basic CRUD operations (core)
- ✓ Share/invite features (viral)
- ✗ Advanced analytics (power user)
- ✗ API access (developer feature)

---

### Tier 1 Rules

**Include if:**
- ✅ Removes key free tier limitations
- ✅ Medium-high adoption (40-80%)
- ✅ Solves primary use case
- ✅ Justifies upgrade from free

**Exclude if:**
- ❌ Niche feature (<40% adoption)
- ❌ Enterprise-only (security, compliance)

**Examples:**
- ✓ Unlimited projects (removes limit)
- ✓ Team collaboration (primary use case)
- ✓ Basic integrations (common need)
- ✗ Advanced permissions (enterprise)
- ✗ SSO (enterprise)

---

### Tier 2 Rules (Target Tier)

**Include if:**
- ✅ Advanced features (power users)
- ✅ Medium adoption (30-60%)
- ✅ Clear value over Tier 1
- ✅ Justifies 2-3x price increase

**Examples:**
- ✓ Advanced analytics/reporting
- ✓ Automation/workflows
- ✓ Premium integrations
- ✓ Custom branding
- ✓ Priority support

**Goal:** Make this tier irresistible to target customers

---

### Tier 3 Rules

**Include if:**
- ✅ Premium features (10-30% adoption)
- ✅ "No limits" positioning
- ✅ Higher scale needs
- ✅ Justifies 3-5x price vs Tier 1

**Examples:**
- ✓ Unlimited everything
- ✓ Advanced customization
- ✓ Premium support
- ✓ Higher rate limits
- ✓ Advanced security (audit logs, etc.)

**Goal:** Best tier for power users, not for everyone

---

### Enterprise Tier Rules

**Include if:**
- ✅ Security/compliance (SSO, SAML, HIPAA)
- ✅ White-glove support (CSM, phone)
- ✅ Custom terms (contracts, SLAs)
- ✅ High-touch needs (onboarding, training)
- ✅ Low adoption (<10%) or high-cost

**Examples:**
- ✓ SSO/SAML
- ✓ Dedicated infrastructure
- ✓ Custom integrations
- ✓ Dedicated CSM
- ✓ 99.99% uptime SLA

**Goal:** Enterprise sales motion, custom pricing

---

## Feature Packaging Checklist

**Per tier, ensure:**

- [ ] **Core value delivered** (can customer achieve main goal?)
- [ ] **Clear upgrade path** (obvious why Tier 2 > Tier 1)
- [ ] **No "frankenstein" tiers** (don't mix unrelated features)
- [ ] **60-70% choose target tier** (Tier 2 most attractive)
- [ ] **Each tier has "hero feature"** (1-2 standout capabilities)

---

## Feature-to-Tier Mapping Table

| Feature | Value | Adoption | Cost | Competitive | Total Score | Assigned Tier |
|---------|-------|----------|------|-------------|-------------|---------------|
| [Feature A] | ___/10 | ___/10 | ___/10 | ___/10 | ___ | Free |
| [Feature B] | ___/10 | ___/10 | ___/10 | ___/10 | ___ | Tier 1 |
| [Feature C] | ___/10 | ___/10 | ___/10 | ___/10 | ___ | Tier 2 |
| [Feature D] | ___/10 | ___/10 | ___/10 | ___/10 | ___ | Tier 3 |
| [Feature E] | ___/10 | ___/10 | ___/10 | ___/10 | ___ | Enterprise |

---

## Validation Testing

### Step 1: Customer Interviews

**Ask customers:**
- "Which features are most valuable to you?" (rank top 5)
- "Which features would you pay more for?"
- "What's missing in [current tier]?"

**Validate:** Are high-value features in right tiers?

---

### Step 2: A/B Testing

**Test feature moves:**
- Move Feature X from Tier 2 → Tier 1
- Measure: Does Tier 1 conversion increase?
- Measure: Does Tier 2 conversion decrease?

**Decision:** Keep if net revenue positive

---

### Step 3: Upgrade Analysis

**Track upgrade paths:**
- Free → Tier 1: What feature triggered upgrade?
- Tier 1 → Tier 2: What feature triggered?

**Optimize:** Ensure gated features are driving upgrades

---

## Common Mistakes

**Mistake 1: Gating core features**
- Don't gate features needed for basic use
- Example: ✗ Limit to 3 tasks in project management tool (can't use product)

**Mistake 2: No clear differentiation**
- Each tier must have obvious value over previous
- Example: ✗ Tier 2 has 10 projects vs Tier 1's 5 (not compelling)

**Mistake 3: Overloading target tier**
- Don't put all features in Tier 2 (no reason to upgrade to Tier 3)

**Mistake 4: Enterprise features in lower tiers**
- Don't include SSO, SAML in Tier 2 (Enterprise won't pay)

---

## Iteration Cycle

**Monthly:**
- Review feature adoption by tier
- Identify under-used features (candidates to move down)
- Identify over-used free features (candidates to gate)

**Quarterly:**
- A/B test feature moves
- Re-validate with customer interviews
- Update tier packaging based on data

---

**Framework owner:** ___________
**Last updated:** ___________
**Next review:** ___________ (recommended: quarterly)
