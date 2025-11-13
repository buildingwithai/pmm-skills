# Pricing Experiment Brief

Template for designing and running pricing tests.

## Experiment Overview

**Experiment name:** ___________
**Owner:** ___________
**Status:** Planning / Running / Complete
**Start date:** ___________
**End date:** ___________

---

## Hypothesis

**Format:** "If we [change], then [metric] will [improve] because [reason]."

**Our hypothesis:**
___________

**Example:** "If we increase Pro tier from $99 to $119, then revenue per visitor will increase by 12% because higher price will outweigh slight conversion drop (expect 5% conversion decrease but 20% price increase = net +12% revenue)."

---

## Context & Rationale

**Why run this experiment:**
[What problem are we solving? What insight led to this hypothesis?]

**Current state:**
- Current price/packaging: ___________
- Current conversion rate: ___%
- Current revenue per visitor: $_____
- Current ACV: $_____

**Expected impact:**
- Expected conversion rate: ___%
- Expected revenue per visitor: $_____
- Expected revenue lift: +___% or $_____ per month

---

## Experiment Design

### What We're Testing

- [ ] Price point ($ amount)
- [ ] Pricing model (per-user, usage-based, etc.)
- [ ] Packaging (feature allocation to tiers)
- [ ] Presentation (CTA copy, tier order, etc.)
- [ ] Discount strategy (annual discount %)
- [ ] Other: ___________

**Specific change:**
- Control: ___________
- Variant: ___________

---

### Test Type

- [ ] A/B test (50/50 split)
- [ ] A/B/n test (multiple variants)
- [ ] Sequential test (time-based, not simultaneous)
- [ ] Multivariate test (multiple variables)

**Traffic split:**
- Control: ___%
- Variant A: ___%
- Variant B: ___ % (if applicable)

---

### Target Audience

**Segment:**
- [ ] All visitors (new customers only)
- [ ] Specific geography: ___________
- [ ] Specific customer size: ___________
- [ ] Trial users only
- [ ] Other: ___________

**Exclusions:**
- [ ] Existing customers (don't change their price)
- [ ] Enterprise (custom pricing, not applicable)
- [ ] Other: ___________

---

## Metrics

### Primary Metric

**Metric:** ___________
**Current baseline:** _____
**Success threshold:** _____ (+___%)

**Why this metric:** [e.g., "Revenue per visitor captures both conversion AND price, so it's the true measure of pricing success"]

---

### Secondary Metrics

**Metric 1:** ___________
- Current: _____
- Target: _____

**Metric 2:** ___________
- Current: _____
- Target: _____

**Metric 3:** ___________
- Current: _____
- Target: _____

---

### Guardrail Metrics

**Metrics we don't want to harm:**

**Guardrail 1: Customer quality (churn rate)**
- Threshold: Don't increase churn by more than ___%

**Guardrail 2: NPS/CSAT**
- Threshold: Don't decrease NPS by more than ___points

**Guardrail 3:** ___________
- Threshold: ___________

---

## Sample Size & Duration

### Statistical Requirements

**Sample size per variation:**
- Minimum: _____visitors (recommended: 250-500)
- Expected traffic: _____visitors/day
- Time to reach sample: _____days

**Statistical significance target:**
- Confidence level: 95% (standard)
- Statistical power: 80%

**Minimum detectable effect (MDE):**
- We can detect a ___% change in primary metric

---

### Test Duration

**Minimum duration:** _____days (recommended: 30-60)
**Maximum duration:** _____days

**Why this duration:**
[e.g., "Need 30 days to capture full month cycle and different visitor cohorts"]

**Date range:** ___________to ___________

---

## Implementation

### Technical Setup

**Tool/platform:**
- [ ] VWO
- [ ] Optimizely
- [ ] Google Optimize
- [ ] Custom (in-house A/B testing)
- [ ] Other: ___________

**Implementation owner:** ___________
**QA owner:** ___________

---

### Steps to Launch

- [ ] Experiment brief approved (this doc)
- [ ] Design variant pricing page/flow
- [ ] Implement A/B test (code, tool setup)
- [ ] QA both variations (control + variant)
- [ ] Configure analytics tracking
- [ ] Set up monitoring dashboard
- [ ] Notify sales/CS teams (if applicable)
- [ ] Launch experiment
- [ ] Monitor first 24 hours for issues

**Launch checklist complete:** Yes / No
**Launch date:** ___________

---

## Monitoring Plan

### Daily Check (First Week)

- [ ] Test running correctly (traffic splitting as expected)
- [ ] No technical issues (errors, broken pages)
- [ ] Tracking working (metrics captured)

**Monitored by:** ___________

---

### Weekly Check

- [ ] Review interim results (don't end test early!)
- [ ] Check for statistical significance
- [ ] Review guardrail metrics (any red flags?)

**Weekly review meeting:** ___________ (day/time)
**Attendees:** ___________

---

### Peeking Problem Warning

⚠️ **Do NOT end test early just because one variation is "winning"** ⚠️

- Early results can be misleading (false positives)
- Run full duration for statistical validity
- Exception: Critical business/technical issue

---

## Decision Criteria

### Success Definition

**Test is successful if:**
- [ ] Primary metric improves by ___% or more
- [ ] Statistical significance reached (p < 0.05)
- [ ] Guardrail metrics not violated

**If successful:** Implement winning variation

---

### Failure Definition

**Test failed if:**
- [ ] Primary metric doesn't improve (or worsens)
- [ ] Guardrail metrics violated (churn increased, etc.)
- [ ] Technical issues prevent valid test

**If failed:** Revert to control, iterate on hypothesis

---

### Inconclusive Result

**Test inconclusive if:**
- [ ] No statistical significance after full duration
- [ ] Results too close to call (<2% difference)

**If inconclusive:**
- [ ] Extend test duration (if feasible)
- [ ] Increase traffic allocation (if possible)
- [ ] Accept null result, move on

---

## Results & Analysis

### Quantitative Results

**Test completion date:** ___________
**Total sample size:** _____ (control: _____, variant: _____)

| Metric | Control | Variant | Change | P-value | Sig? |
|--------|---------|---------|--------|---------|------|
| **Primary: _____** | _____ | _____ | _____% | _____ | Yes/No |
| Secondary: _____ | _____ | _____ | _____% | _____ | Yes/No |
| Secondary: _____ | _____ | _____ | _____% | _____ | Yes/No |
| Guardrail: _____ | _____ | _____ | _____% | _____ | Yes/No |

**Winner:** Control / Variant A / Inconclusive

**Confidence level:** ___%

---

### Qualitative Feedback

**Customer feedback (if any):**
- Support tickets: _____related to test
- Sales team input: ___________
- Customer comments: ___________

**Key insights:**
1. ___________
2. ___________
3. ___________

---

### Segment Analysis

**Did results vary by segment?**

| Segment | Control | Variant | Change | Insight |
|---------|---------|---------|--------|---------|
| SMB | _____ | _____ | _____% | _____ |
| Mid-market | _____ | _____ | _____% | _____ |
| Enterprise | _____ | _____ | _____% | _____ |

**Segmentation insight:**
[e.g., "Variant performed 20% better with SMB, but 10% worse with enterprise → consider different pricing by segment"]

---

## Decision & Next Steps

### Recommendation

- [ ] **Implement variant** (winning variation becomes new default)
- [ ] **Keep control** (current pricing stays)
- [ ] **Iterate & retest** (learnings lead to new hypothesis)

**Rationale:**
___________

---

### Rollout Plan (if implementing)

**Implementation timeline:**
- Week 1: Update pricing page
- Week 2: Update billing system
- Week 3: Train sales/CS teams
- Week 4: Launch to 100% of traffic

**Migration plan:**
- [ ] New customers only (existing customers grandfathered)
- [ ] All customers (universal migration)

**Communication plan:**
- [ ] Internal announcement (sales, CS, support)
- [ ] External announcement (blog post, email if price increase)

**Rollout owner:** ___________
**Target date:** ___________

---

### Follow-Up Monitoring

**Post-launch metrics to track:**
- Conversion rate (first 30 days)
- Revenue impact (first 90 days)
- Churn rate (first 6 months)

**Review date:** ___________

---

### Learnings & Iteration

**What we learned:**
1. ___________
2. ___________
3. ___________

**What surprised us:**
___________

**Next experiment:**
[Based on learnings, what should we test next?]
___________

---

## Appendix

### Screenshots

- [ ] Control variation screenshot
- [ ] Variant variation screenshot

### Data Access

- Experiment dashboard: [URL]
- Raw data export: [Location]
- Analytics report: [Link]

### Stakeholder Sign-Off

**Approved by:**
- [ ] Product Marketing
- [ ] Product Management
- [ ] Finance (if significant revenue impact)
- [ ] CRO/VP Sales (if affects sales)

**Approval date:** ___________

---

**Experiment owner:** ___________
**Last updated:** ___________
**Status:** Planning / Running / Complete / Implemented
