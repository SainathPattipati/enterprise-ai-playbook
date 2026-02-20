# Predictive Maintenance Playbook

## Overview

Predictive maintenance is the most common manufacturing AI use case for good reason: high ROI, well-understood data, and immediate operational impact.

## The Problem

**Current state (reactive maintenance):**
- Equipment fails → production stops → $50K-500K/hour downtime
- Maintenance scheduled on calendar (even if equipment is fine)
- No visibility into equipment health until failure occurs

**Opportunity:**
- Predict failure 2-4 weeks in advance
- Schedule maintenance during planned downtime
- Shift from reactive to proactive
- Reduce total maintenance costs despite more frequent service

## Success Metrics

| Metric | Baseline | Target | Impact |
|--------|----------|--------|--------|
| Unplanned downtime | 20 hrs/month | 3 hrs/month | $10.2M saved/year |
| Equipment MTBF | 1500 hours | 4000+ hours | Extended life |
| Maintenance costs | $400K/month | $380K/month | Lower total cost |
| Maintenance crew utilization | 65% | 85% | Better resource use |

## Data Requirements

You'll need:
- **Equipment sensor data:** Temperature, vibration, pressure, RPM
- **Maintenance logs:** When did failures occur? What was repaired?
- **Equipment specifications:** Model, age, operating hours
- **Ambient conditions:** Plant temperature, humidity

## Implementation Roadmap

### Phase 1: Foundation (Weeks 1-4)
- Audit sensors on critical equipment (top 5 failure drivers)
- Collect 3-6 months of historical data
- Document all failure patterns
- Assess data quality

### Phase 2: Baseline Model (Weeks 5-12)
Build a baseline model:
- 80% threshold-based rules
- 20% statistical anomaly detection
- Target: 70-75% accuracy

### Phase 3: Advanced Models (Weeks 13-20)
- Transition to ML models (Random Forest, XGBoost)
- Target: 85%+ accuracy

### Phase 4: Production & Monitoring (Week 21+)
- Deploy to operations
- Set up automated alerts
- Establish maintenance workflows
- Monitor for model drift monthly

## Critical Success Factors

### 1. Get the Right Equipment
Target equipment with:
- High failure frequency (3+ failures/year)
- High downtime cost (>$100K per failure)
- Rich sensor data available
- Clear failure signatures

### 2. Validate with Maintenance Team
Work with the people who maintain equipment:
- What are their concerns?
- What would make maintenance easier?
- What false alarms can they tolerate?

Early dismissal from maintenance kills adoption.

### 3. Clean the Sensor Data
80% of your effort. Real challenges:
- Sensor dropouts (missing data)
- Sensor calibration drift
- Different firmware versions
- Environmental interference

### 4. Define "Failure" Clearly
Is it when something breaks completely, when performance drops >10%, or when we schedule maintenance?

Work with operations to define exactly what you're predicting.

### 5. Establish Confidence Thresholds
You'll get probability scores. At what probability do you alert maintenance?

Answer depends on false alarm cost:
- High tolerance for false alarms? Alert at 60% confidence
- Low tolerance? Alert at 85% confidence

Run 8-week pilot to find the right threshold.

## Common Pitfalls

### Pitfall 1: Predicting Too Far Ahead
"Let's predict failures 6 months in advance!"

**Reality:** Sensor data predicts failures 2-4 weeks out with high confidence.

### Pitfall 2: Ignoring External Factors
Failure modes change with operator skill, ambient temperature, material quality, etc.

**Fix:** Include external variables in your model.

### Pitfall 3: One Model Fits All
Equipment ages differently and operates differently.

**Fix:** Build equipment-specific or line-specific models (10-20 variants).

### Pitfall 4: Forgetting About Maintenance Actions
When you do preventive work, you prevent failure. Your model can't see this.

**Fix:** Feed maintenance actions back into the data.

## Model Selection Guide

| Approach | Accuracy | When to Use |
|----------|----------|------------|
| Threshold Rules | 60% | Baseline/pilot |
| Isolation Forest | 75% | Anomaly detection |
| Random Forest | 82% | Production workhorse |
| XGBoost | 85% | When accuracy critical |
| LSTM (time series) | 87% | When temporal patterns matter |

**Recommendation:** Start with Random Forest. Explainability is critical for adoption.

## Deployment Checklist

- [ ] Model accuracy >80% on holdout test set
- [ ] False alarm rate acceptable to maintenance (<30%)
- [ ] Production data pipeline tested
- [ ] Alert delivery mechanism established
- [ ] Maintenance workflow updated
- [ ] Operations team trained
- [ ] Monitoring & retraining plan documented
- [ ] Escalation process for high-confidence alerts defined
- [ ] Model versioning and rollback procedure ready

## Year 1 Outcomes to Expect

**Optimistic:**
- 40% reduction in unplanned downtime
- 15% reduction in total maintenance costs
- 2+ successful pilots scaled

**Realistic:**
- 25% reduction in unplanned downtime
- Flat total costs
- 1 successful pilot

**Pessimistic:**
- 10% reduction in downtime
- No cost reduction
- Model concerns

## Next Steps

1. **Week 1:** Identify candidate equipment
2. **Week 2:** Collect sensor and maintenance data
3. **Week 3:** Meet with maintenance team
4. **Week 4:** Start baseline model
5. **Week 12:** Evaluate baseline with operations
6. **Week 16:** Begin advanced model development
7. **Week 24:** Pilot deployment
8. **Month 7+:** Scale to additional equipment

---

Predictive maintenance works because it solves a real problem with data that already exists.
