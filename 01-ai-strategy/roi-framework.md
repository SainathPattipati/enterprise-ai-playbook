# ROI Framework for Enterprise AI

## The Problem with AI ROI

"How much will AI save us?" is the question every CFO asks. Most AI teams struggle to answer it. This framework changes that.

**Key insight:** Most of your value is "soft" (efficiency, speed, quality). Force yourself to monetize the soft stuff.

## Three Types of Value

### 1. Hard Savings
**Direct cost reduction. Easiest to measure.**

Examples:
- Reduce defects by 5% → directly lower scrap costs
- Predict equipment failure 2 weeks early → avoid $500K downtime
- Automate data entry → save FTE headcount

**Formula:**
```
Hard Savings = (Current Cost) - (Cost with AI)
```

### 2. Soft Benefits
**Efficiency, speed, quality improvements that have economic value.**

Examples:
- Faster decision-making (reduce time-to-insight from 4 hours to 15 min)
- Better quality (fewer customer complaints)
- Improved utilization (run equipment 5% longer before maintenance)

**Formula:**
```
Soft Benefit Value = (Hours Saved) × (Hourly Rate) × (Annual Frequency)
```

### 3. New Revenue
**New business enabled by AI. Hardest to predict but highest upside.**

Examples:
- Personalized product recommendations (increase customer lifetime value 15%)
- Predictive analytics service (new line of business)
- Real-time optimization (open new market segments)

**Formula:**
```
New Revenue = (New Customer Segment Size) × (Average Deal Size) × (Conversion Rate)
```

## Building Your ROI Model

### Step 1: Define the Current State

**Example: Predictive Maintenance**

Current state:
- Equipment downtime: 20 hours/month per plant
- Cost of downtime: $50,000/hour
- 5 plants = $5M annual downtime cost
- Current maintenance: reactive only

### Step 2: Define the AI Improvement

"What changes when we deploy AI?"

For predictive maintenance:
- **Prediction Accuracy:** 85% (catch 85% of failures before they happen)
- **False Positive Rate:** 15% (trigger unnecessary maintenance 15% of the time)
- **Lead Time:** 2 weeks (can schedule maintenance before failure)

### Step 3: Model the Impact

**Unplanned downtime reduction:**
- Current: 20 hours/month
- Prevented failures: 20 × 0.85 = 17 hours/month
- Net prevention: 17 - (false positives impact) = 15 hours/month
- Annual savings: 15 hours × $50K × 12 = $9M/year

**Increased maintenance costs:**
- Preventive maintenance: 5 extra hours/month × $5K/hour
- False positive cost: $10K × (false positive count)
- Annual cost: $300K/year

**Net ROI per plant:**
```
($9M - $300K) / Plant Cost
```

### Step 4: Account for Soft Benefits

What else improves?

- **Equipment lifespan:** Better maintenance extends life by 2 years
  - Value: (Equipment replacement cost) / (Current lifespan) × 2 years
  
- **Operator utilization:** Less time troubleshooting
  - Value: (Operator hours freed) × (Hourly rate)
  
- **Quality:** Better maintained equipment produces higher quality
  - Value: (Quality improvement %) × (Product margin)

### Step 5: Calculate Total ROI

```
Total Annual Value = Hard Savings + Soft Benefits + New Revenue
Implementation Cost = Model Development + Infrastructure + Training
ROI = (Total Annual Value - Implementation Cost) / Implementation Cost
Payback Period = Implementation Cost / Annual Value
```

## Real Example: Demand Forecasting

### Current State
- Annual inventory carrying cost: $2M
- Forecast error: ±15% (causes over/under-stock)
- Planning cycle: 3 months
- New product launches: miss 30% of demand

### With AI Forecasting
- Model accuracy: 93% (reduce error to ±7%)
- Planning cycle: 1 month (faster reforecasting)
- New product launches: capture 80% of demand

### Value Calculation

| Item | Calculation | Annual Value |
|------|-------------|--------------|
| Reduced inventory | (Error %) × $2M | $1,600,000 |
| Prevented stockouts | 15% revenue increase on new launches | $400,000 |
| Operational efficiency | Faster planning = 2 FTE saved | $300,000 |
| Cash flow improvement | Better working capital | $200,000 |
| **Total Value** | | **$2,500,000** |

**Implementation Cost:** $400,000 (model development, data, infrastructure)

**ROI:** 525% Year 1
**Payback:** 2 months

## Common ROI Mistakes

### Mistake 1: Comparing to Perfection
"AI is 90% accurate, humans are 95%"

**Reality:** Humans don't do this work consistently. Their accuracy varies 60-85% depending on fatigue, experience, etc.

**Fix:** Benchmark against actual human performance, not theoretical maximum.

### Mistake 2: Forgetting Implementation Costs
"Model costs $50K, saves $500K"

**Reality:** You need infrastructure, training, change management, ongoing monitoring = $200K additional cost

**Fix:** Account for full cost of ownership including salaries for maintaining models.

### Mistake 3: Ignoring Adoption Risk
"50% adoption in year 1, 100% in year 2"

**Reality:** 30% adoption is optimistic. Many pilots never scale.

**Fix:** Build adoption risk into your model. Conservative assumptions:
- Year 1: 20% adoption
- Year 2: 50% adoption
- Year 3: 75% adoption

### Mistake 4: Not Accounting for Model Drift
"Model stays accurate forever"

**Reality:** Model accuracy degrades over time (data distribution changes)

**Fix:** Budget 10-20% annual effort for model retraining and monitoring.

## Communicating ROI to Leadership

### For CFO (Focus on Money)
```
Annual Savings: $2.5M
Implementation Cost: $400K
Year 1 ROI: 525%
Payback: 2 months
```

### For COO (Focus on Operations)
```
- Reduce equipment downtime from 20 to 5 hours/month
- Improve forecast accuracy from ±15% to ±7%
- Free up 3 FTEs for higher-value work
```

### For CEO (Focus on Strategy)
```
- Enables 15% faster decision-making across operations
- Positions us as technology leader in manufacturing
- Competitive advantage from AI-driven optimization
```

## ROI Monitoring Dashboard

Track these quarterly:

| Metric | Target | Actual | Variance |
|--------|--------|--------|----------|
| Model accuracy | 92% | 89% | -3% |
| System uptime | 99.9% | 99.5% | -0.4% |
| Adoption rate | 50% | 35% | -15% |
| Annual savings | $2.5M | $1.2M | -52% |
| Model cost/month | $5K | $7K | +40% |

**When variance > 20%:** Investigate and correct

## Keys to Credible ROI

1. **Use conservative estimates** — Under-promise, over-deliver
2. **Track everything** — Measure actual outcomes vs projections
3. **Update quarterly** — Your ROI model should evolve
4. **Be honest about failures** — "This model isn't delivering value, here's why"
5. **Attribute value carefully** — Don't claim credit for other projects' outcomes
6. **Include all costs** — Infrastructure, people, training, maintenance

## Getting Started

1. Define your current state with actual numbers
2. Identify 3-5 specific improvements AI will deliver
3. Build conservative financial model
4. Validate assumptions with operational leaders
5. Set up tracking dashboard
6. Review and adjust quarterly

---

**Remember:** The goal is not to prove AI is magical. It's to build trust that AI investments will deliver measurable, sustained value.
