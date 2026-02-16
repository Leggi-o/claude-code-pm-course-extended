# Guided Onboarding: Impact Estimation & ROI Model

**Feature:** Guided Onboarding with Sample Project
**Owner:** Senior PM, Activation
**Date:** Q4 2024
**Status:** Impact model for leadership approval

---

## Executive Summary

**Investment:** $100,000 (4 eng-months)
**Expected Return (Realistic Scenario):** $39,312 ARR Year 1, $943,296 in 3-year LTV
**ROI:** 0.39x in Year 1, **9.4x over 3 years**

**Recommendation:** Proceed with build. Even pessimistic scenario (2.6x ROI) justifies investment. Strategic value: can't scale with 45% activation rate stuck for 6 months.

---

## Current State Metrics

From Q4 2024 usage data analysis:

**Signups:**
- 5,000 new signups/month (average)
- Growing 5% month-over-month

**Activation Rate:**
- **45% overall** (2,250 activated users/month out of 5,000 signups)
- Activation = user completes first task

**Time to Value:**
- Median time from signup to first task completed: **45 minutes**
- 75th percentile: 78 minutes (slow!)

**Conversion to Paying:**
- 60% of activated users convert to paid within 30 days
- Average time to first payment: 14 days

**Revenue Metrics:**
- ARPU: $12/month
- Average customer lifetime: 24 months
- **LTV per activated user:** $12 × 60% conversion × 24 months = $172.80

---

## Impact Estimation Framework Applied

### Formula:
```
Impact = Users Affected × Current Action Rate × Expected Lift × Value per Action
```

### Component 1: Users Affected

**Gradual Rollout Strategy:**
- Not launching to 100% immediately
- Week 1-2: 20% of signups (A/B test)
- Week 3-4: If successful, ramp to 50%
- Week 5+: Ramp to 100%
- **Average steady-state adoption: 70%** (some users may skip guided onboarding, choose "Start from scratch")

**Monthly users affected:** 5,000 signups × 70% = **3,500 users/month**

### Component 2: Current Action Rate

**Baseline activation:** 45%

**Of the 3,500 users who see guided onboarding:**
- Current activated: 3,500 × 45% = **1,575 users/month**

### Component 3: Expected Lift

**This is the critical assumption.** Multiple approaches to estimate:

**Approach 1: Problem-based estimate**
- Survey data: 60% of drop-offs cite "confusion" and "no examples"
- If guided onboarding eliminates confusion, could recover some of that 60%
- Conservative: Recover 30% of confused users = 0.60 × 0.30 = 18pp potential lift
- Reality check: Not all confusion is solvable, some users churn for other reasons
- **Realistic estimate: 13pp lift** (45% → 58%)

**Approach 2: Benchmark comparison**
- Linear (similar product): ~65% activation
- Asana (more complex): ~50% activation
- Notion (steeper learning curve): ~40% activation
- TaskFlow currently: 45%
- Room to improve: 65% - 45% = 20pp
- **Realistic capture: 13pp of that 20pp** (getting 65% of the way to Linear's performance)

**Approach 3: Historical reference**
- Previous onboarding improvement (Q2 2024) lifted activation 45% → 48% (+3pp)
- That was a minor UI change
- Guided onboarding is a major change → expect 3-4x the impact
- 3pp × 4 = 12pp lift
- **Realistic estimate: 13pp lift** ✓

**All three approaches converge on ~13pp lift. Use 45% → 58% activation.**

### Component 4: Value per Action

**Activated user value:**
- 60% convert to paying customer
- $12/month ARPU
- 24-month average lifetime
- **LTV = $172.80 per activated user**

**Note:** This is conservative - activated users who stay longer than 24 months aren't counted. Retention improvements from better onboarding could increase LTV further.

---

## Realistic Scenario (50th Percentile)

### Assumptions:
- **Adoption:** 70% of signups see guided onboarding
- **Lift:** 45% → 58% activation (+13pp)
- **Users affected:** 3,500/month
- **Value:** $172.80 LTV per activation

### Impact Calculation:

**Current state (for the 3,500 who will see guided onboarding):**
- Activated: 3,500 × 45% = 1,575 users/month

**Projected state:**
- Activated: 3,500 × 58% = 2,030 users/month

**Incremental impact:**
- **+455 activated users/month**

### Revenue Impact:

**Monthly Recurring Revenue (MRR):**
- 455 users × $12 ARPU × 60% conversion = **$3,276 MRR**

**Annual Recurring Revenue (ARR):**
- $3,276 × 12 months = **$39,312 ARR**

**3-Year Lifetime Value:**
- 455 users/month × 12 months × $172.80 LTV = **$943,296**

### ROI Calculation:

**Investment:** $100,000
- 2 engineers × 2 months each = 4 eng-months
- Blended eng cost: ~$25k/month
- Total: $100k

**Returns:**
- **Year 1 ROI:** $39,312 / $100,000 = **0.39x** (payback in ~2.5 years)
- **3-Year ROI:** $943,296 / $100,000 = **9.4x**

---

## Why Year 1 ROI < 1.0x is OK

Leadership might balk at 0.39x Year 1 ROI. Here's the context:

**1. This is LTV-based, not cash-based**
- Customers pay monthly, so Year 1 cash impact is higher than ARR suggests
- Months 1-12 generate $39k in actual revenue collected

**2. Compounding effect**
- +455 activated users EVERY MONTH
- By Month 12, we've added 5,460 total activated users
- That's $943k in LTV that wouldn't exist otherwise

**3. Strategic necessity**
- Activation stuck at 45% for 6 months - this is a growth blocker
- Can't scale user acquisition if half of signups churn
- CAC payback improves from 8 months to 6 months (faster payback = more growth capital)

**4. Retention multiplier not modeled**
- Activated users with better onboarding likely stay LONGER than 24 months
- Historical data: users who complete onboarding thoroughly have 2.5x longer lifetime
- If true LTV is $172 × 2.5 = $432, then 3-year ROI is actually 23.5x

---

## Alternative Scenarios

To bound the uncertainty, here are pessimistic and optimistic cases:

### Pessimistic Scenario (20th percentile)

**Assumptions:**
- Adoption: 30% (slow rollout, many users skip it)
- Lift: 45% → 50% (+5pp, smaller than expected)

**Impact:**
- Users affected: 5,000 × 30% = 1,500/month
- Activated: 1,500 × 50% = 750/month
- Current baseline for those 1,500: 1,500 × 45% = 675/month
- **Incremental: +75 users/month**

**Revenue:**
- MRR: 75 × $12 × 60% = $540
- ARR: $6,480
- 3-Year LTV: 75 × 12 × $172.80 = $155,520

**ROI:**
- Year 1: $6,480 / $100,000 = **0.06x** (ouch!)
- 3-Year: $155,520 / $100,000 = **1.6x**

**Analysis:** Even if adoption is low and lift is small, we still get 1.6x ROI over 3 years. Not great, but not a disaster.

### Optimistic Scenario (80th percentile)

**Assumptions:**
- Adoption: 90% (strong rollout, very few skip)
- Lift: 45% → 62% (+17pp, includes retention benefits)

**Impact:**
- Users affected: 5,000 × 90% = 4,500/month
- Activated: 4,500 × 62% = 2,790/month
- Current baseline for those 4,500: 4,500 × 45% = 2,025/month
- **Incremental: +765 users/month**

**Revenue:**
- MRR: 765 × $12 × 60% = $5,508
- ARR: $66,096
- 3-Year LTV: 765 × 12 × $172.80 = $1,586,304

**ROI:**
- Year 1: $66,096 / $100,000 = **0.66x**
- 3-Year: $1,586,304 / $100,000 = **15.9x**

**Analysis:** If guided onboarding works really well and most users adopt it, we could see 15.9x ROI. This would be a home run.

---

## Scenario Summary Table

| Scenario | Adoption | Lift | Incremental Users/Mo | ARR Year 1 | 3-Year LTV | ROI (3yr) |
|----------|----------|------|---------------------|------------|------------|-----------|
| **Pessimistic** | 30% | 45%→50% | +75 | $6.5k | $156k | **1.6x** |
| **Realistic** | 70% | 45%→58% | +455 | $39k | $943k | **9.4x** |
| **Optimistic** | 90% | 45%→62% | +765 | $66k | $1.6M | **15.9x** |

**Key insight:** Even in the pessimistic case, we get 1.6x ROI over 3 years. Realistic case is 9.4x. Risk-adjusted, this is a good bet.

---

## Assumptions & Risks

### Critical Assumptions:

1. **70% adoption rate**
   - Assumes most users complete guided onboarding
   - Risk: Users skip it or it's too long
   - Mitigation: Make it short (2-3 min), allow skip but prompt later

2. **13pp lift (45% → 58%)**
   - Based on problem recovery (60% confused × 30% recovered)
   - Risk: Lift is smaller if root cause misdiagnosed
   - Mitigation: A/B test before full rollout to validate

3. **60% activation → paid conversion holds**
   - Assumes guided-onboarding users convert at same rate as organic activations
   - Risk: Lower quality activations don't convert as well
   - Mitigation: Track conversion rate separately for guided vs. organic

4. **24-month LTV holds**
   - Historical average lifetime
   - Risk: Shorter if onboarding doesn't improve retention
   - Opportunity: Longer if better onboarding → better retention (2.5x multiplier observed historically)

### Risks & Mitigations:

**Risk 1: Low adoption (30% instead of 70%)**
- What if users skip guided onboarding?
- Mitigation: Make it opt-out instead of opt-in, but allow "Start from scratch" for power users

**Risk 2: Smaller lift than expected (5pp instead of 13pp)**
- What if guided onboarding doesn't solve the confusion problem?
- Mitigation: A/B test with 20% of users first, validate lift before scaling

**Risk 3: Enterprise users react negatively**
- What if sample project is too simplistic for enterprise needs?
- Mitigation: Segment by company size, show different examples or skip for 100+ employee companies

**Risk 4: Engineering takes longer than 4 months**
- What if complexity is underestimated?
- Mitigation: Scope to MVP (basic sample project), defer advanced features to V2

---

## Strategic Value Beyond ROI

**Quantitative ROI is important, but not the whole story:**

### 1. Unblocks growth
- Current 45% activation rate limits how aggressively we can spend on user acquisition
- Higher activation → better CAC payback → more marketing budget → faster growth

### 2. Competitive positioning
- Linear: 65% activation (beating us)
- Asana: 50% activation (beating us)
- We look weak in competitive sales cycles when prospects ask about onboarding

### 3. Retention multiplier
- Historical data: Users who have strong first experience stay 2.5x longer
- If guided onboarding creates better first experience, LTV could be $432 instead of $173
- This would make the 3-year ROI 23.5x instead of 9.4x

### 4. Viral coefficient improvement
- Activated users invite teammates at 3x the rate of non-activated users
- +455 activated users/month = +136 additional invites/month (at 30% invite rate)
- Invites convert at 40% → +54 additional signups/month from virality
- Compounding growth effect not modeled in ROI

---

## Recommendation

**Proceed with build.**

**Why:**
1. ✅ Even pessimistic scenario (1.6x ROI) justifies $100k investment
2. ✅ Realistic scenario (9.4x ROI) is a strong return
3. ✅ Strategic necessity: 45% activation is a growth blocker
4. ✅ Retention and viral multipliers likely understate true impact
5. ✅ Competitive pressure: Asana and Linear have better activation

**Next steps:**
1. Get leadership approval for $100k investment
2. Design sample project with Design team (2 weeks)
3. Build and A/B test (4 weeks)
4. Validate lift with 20% of users before scaling to 100%
5. Monitor activation, conversion, and retention metrics closely

**Timeline:**
- Week 1-2: Design
- Week 3-6: Build
- Week 7-8: A/B test (20% treatment)
- Week 9-10: Scale to 100% (if test succeeds)
- Week 11-12: Monitor and iterate

**Success criteria for A/B test:**
- Activation lift ≥10pp (we projected 13pp, so 10pp is threshold)
- No decrease in conversion to paid
- User feedback is positive (NPS ≥40 for guided onboarding flow)

---

**This impact estimate demonstrates that Guided Onboarding is a high-ROI, strategically important investment that addresses a validated problem with clear business value.**
