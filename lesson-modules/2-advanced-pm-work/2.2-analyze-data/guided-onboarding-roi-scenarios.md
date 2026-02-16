# Guided Onboarding: ROI Scenario Analysis

**Feature:** Guided Onboarding with Sample Project
**Purpose:** Show leadership the range of possible outcomes
**Investment:** $100,000 (4 eng-months)

---

## Why Three Scenarios?

Single-point estimates are dangerous because they:
- Hide uncertainty
- Create false precision
- Don't help leadership understand risk
- Lead to disappointment when reality doesn't match the estimate

**Three scenarios show:**
- ✅ Best case (things go really well)
- ✅ Most likely case (realistic expectations)
- ✅ Worst case (what if it underperforms)

This helps leadership make an informed decision about the $100k investment.

---

## Key Assumptions to Vary

1. **Adoption rate:** What % of users see/complete guided onboarding?
2. **Activation lift:** How much does activation improve?
3. **Secondary effects:** Retention improvements, viral growth, etc.

---

## Scenario 1: Pessimistic (20th percentile - Things Go Poorly)

### Assumptions:
- **Adoption:** 30% (slow rollout, many users skip it, or we pause rollout early)
- **Lift:** 45% → 50% activation (+5pp instead of +13pp)
- **Why:** Sample project doesn't resonate, users find it confusing, or root cause was misdiagnosed

### Impact Calculation:

**Users affected:** 5,000 signups/month × 30% = 1,500/month

**Current baseline (for those 1,500):**
- 1,500 × 45% = 675 activated/month

**Projected (with guided onboarding):**
- 1,500 × 50% = 750 activated/month

**Incremental impact:** +75 activated users/month

### Revenue Impact:

**Year 1 (12 months of adding +75 users/month):**
- Total users added: 75 × 12 = 900 users
- Incremental revenue Year 1: ~$78k (cash collected, triangular ramp)
- End-of-year ARR run-rate: 900 × $7.20/mo × 12 = $77,760

**3-Year LTV:**
- Total users added over 36 months: 75 × 36 = 2,700 users
- LTV: 2,700 × $172.80 = $466,560

### ROI:

- **Year 1 ROI:** $78k / $100k = **0.78x** (close to breakeven)
- **3-Year ROI:** $467k / $100k = **4.7x**

### Analysis:

Even if adoption is low and lift is small, we still get:
- ✅ Payback in ~15 months
- ✅ 4.7x ROI over 3 years
- ✅ Some improvement to activation (better than status quo)

**Conclusion:** Not great, but not a disaster. Still worth doing.

---

## Scenario 2: Realistic (50th percentile - Expected Case)

### Assumptions:
- **Adoption:** 70% (gradual rollout, most users see it)
- **Lift:** 45% → 58% activation (+13pp)
- **Why:** Based on problem recovery math (60% confused × 30% recovered) + benchmark comparisons

### Impact Calculation:

**Users affected:** 5,000 signups/month × 70% = 3,500/month

**Current baseline (for those 3,500):**
- 3,500 × 45% = 1,575 activated/month

**Projected (with guided onboarding):**
- 3,500 × 58% = 2,030 activated/month

**Incremental impact:** +455 activated users/month

### Revenue Impact:

**Year 1 (12 months of adding +455 users/month):**
- Total users added: 455 × 12 = 5,460 users
- Incremental revenue Year 1: ~$470k (cash collected)
- End-of-year ARR run-rate: 5,460 × $7.20/mo × 12 = $472,032

**3-Year LTV:**
- Total users added over 36 months: 455 × 36 = 16,380 users
- LTV: 16,380 × $172.80 = $2,830,464

### ROI:

- **Year 1 ROI:** $470k / $100k = **4.7x** ✓
- **3-Year ROI:** $2.83M / $100k = **28.3x** ✓

### Analysis:

This is our expected case:
- ✅ Strong Year 1 payback (5 months)
- ✅ Excellent 3-year ROI (28.3x)
- ✅ Moves activation from 45% → 58% (gets us competitive with Linear at 65%)

**Conclusion:** Strong business case. High confidence this is achievable.

---

## Scenario 3: Optimistic (80th percentile - Things Go Great)

### Assumptions:
- **Adoption:** 90% (strong rollout, very few skip, becomes default experience)
- **Lift:** 45% → 62% activation (+17pp)
- **Why:** Sample project resonates extremely well, PLUS secondary effects:
  - Better onboarding → higher retention (users stay 2.5x longer)
  - Activated users invite teammates more (viral growth)
  - Quality of activations improves (higher conversion to paid)

### Impact Calculation:

**Users affected:** 5,000 signups/month × 90% = 4,500/month

**Current baseline (for those 4,500):**
- 4,500 × 45% = 2,025 activated/month

**Projected (with guided onboarding):**
- 4,500 × 62% = 2,790 activated/month

**Incremental impact:** +765 activated users/month

### Revenue Impact:

**Year 1 (12 months of adding +765 users/month):**
- Total users added: 765 × 12 = 9,180 users
- Incremental revenue Year 1: ~$790k (cash collected)
- End-of-year ARR run-rate: 9,180 × $7.20/mo × 12 = $793,152

**3-Year LTV (with retention multiplier):**
- Total users added over 36 months: 765 × 36 = 27,540 users
- Base LTV: 27,540 × $172.80 = $4,758,912
- With 2.5x retention multiplier: $4,758,912 × 1.5 = **$7,138,368**
  - (Note: Multiplier is 1.5x not 2.5x because baseline LTV already includes some retention)

### ROI:

- **Year 1 ROI:** $790k / $100k = **7.9x**
- **3-Year ROI (with retention boost):** $7.14M / $100k = **71.4x** 🚀

### Analysis:

If everything goes right:
- ✅ Payback in ~6 weeks (!)
- ✅ Massive 71.4x ROI over 3 years
- ✅ Activation jumps to 62% (best-in-class, beating Linear)
- ✅ Retention improvements compound the value

**Conclusion:** Home run scenario. Low probability but high upside.

---

## Scenario Comparison Table

| Metric | Pessimistic | Realistic | Optimistic |
|--------|-------------|-----------|------------|
| **Adoption** | 30% | 70% | 90% |
| **Lift** | +5pp (45%→50%) | +13pp (45%→58%) | +17pp (45%→62%) |
| **Incremental Users/Mo** | +75 | +455 | +765 |
| **Year 1 Revenue** | $78k | $470k | $790k |
| **Year 1 ROI** | 0.78x | 4.7x | 7.9x |
| **3-Year LTV** | $467k | $2.83M | $7.14M |
| **3-Year ROI** | **4.7x** | **28.3x** | **71.4x** |
| **Payback Period** | 15 months | 2.5 months | 1.5 months |

---

## Risk-Adjusted Expected Value

If we assign probabilities to each scenario:
- Pessimistic: 20% chance
- Realistic: 60% chance
- Optimistic: 20% chance

**Expected 3-Year ROI:**
- (0.20 × 4.7x) + (0.60 × 28.3x) + (0.20 × 71.4x) = **32.2x expected ROI**

Even accounting for risk, the expected return is **32.2x** - an excellent investment.

---

## Key Insights from Scenario Analysis

### 1. **Downside is manageable**
- Even pessimistic case gets 4.7x ROI over 3 years
- We don't lose money in any scenario
- Worst case = slow payback but still profitable

### 2. **Upside is massive**
- Optimistic case is 71.4x ROI
- Retention multiplier (not modeled in realistic case) could add significant value
- Viral growth from better-activated users compounds over time

### 3. **Realistic case is strong**
- 28.3x ROI over 3 years
- Supported by multiple lines of evidence (problem recovery, benchmarks, historical data)
- Conservative assumptions (e.g., no retention boost modeled)

### 4. **Risk/reward is favorable**
- **Downside:** 4.7x ROI (acceptable)
- **Most likely:** 28.3x ROI (excellent)
- **Upside:** 71.4x ROI (exceptional)
- **Asymmetric bet:** Limited downside, massive upside

---

## What Could Move Us Between Scenarios?

**From Realistic → Pessimistic:**
- ❌ Users skip guided onboarding (opt-out rate >50%)
- ❌ Sample project confuses more than it helps
- ❌ Enterprise users react negatively, we pause rollout
- ❌ Engineering takes 6 months instead of 4 (delays, reduces ROI)

**From Realistic → Optimistic:**
- ✅ Sample project becomes viral (users share screenshots, request features based on it)
- ✅ Activated users stay significantly longer (retention multiplier)
- ✅ Guided onboarding becomes the default experience (95%+ adoption)
- ✅ We discover secondary benefits (better feature adoption, more team invites)

---

## Recommendation to Leadership

**Proceed with build.**

**Why:**
1. ✅ **Even pessimistic scenario (4.7x ROI) justifies investment**
   - No scenario loses money
   - Downside risk is acceptable
2. ✅ **Realistic scenario (28.3x ROI) is well-supported**
   - Three independent estimation approaches converge on ~13pp lift
   - Conservative assumptions (no retention boost, no viral effect)
3. ✅ **Risk/reward asymmetry favors action**
   - Limited downside, massive upside
   - Optionality: Can pause rollout if A/B test shows pessimistic results
4. ✅ **Strategic necessity**
   - 45% activation is a growth blocker
   - Can't scale marketing spend with poor activation
   - Competitive pressure (Linear 65%, Asana 50%, we're 45%)

**De-risk with phased rollout:**
- Week 1-2: A/B test with 20% of users
- Measure actual lift - if ≥10pp, proceed to realistic scenario
- If <5pp, pause and investigate (pessimistic scenario)
- Built-in checkpoints prevent downside scenario

**Expected outcome:** Realistic scenario (28.3x ROI over 3 years)

---

## Next Steps

1. ✅ **Get leadership approval** (use this scenario analysis)
2. ⏭️ **Design sample project** with Design team
3. ⏭️ **Build & A/B test** (4 weeks build, 2 weeks test)
4. ⏭️ **Measure actual results** against scenarios
5. ⏭️ **Update forecast** based on real data
6. ⏭️ **Scale to 100%** if A/B test validates realistic case

---

**This scenario analysis gives leadership the full picture: best case, most likely case, and worst case. The range of outcomes (4.7x to 71.4x ROI) shows this is a high-conviction bet with manageable downside and exceptional upside.**
