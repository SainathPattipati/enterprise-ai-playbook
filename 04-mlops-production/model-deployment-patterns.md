# Model Deployment Patterns

Safe ways to deploy ML models to production.

## Pattern 1: Blue-Green Deployment

Run two identical environments. Switch traffic between them.

**How it works:**
1. Current model running in "Blue" environment
2. Deploy new model to "Green" environment
3. Test Green thoroughly
4. Switch traffic from Blue to Green
5. Keep Blue as instant rollback

**Pros:**
- Zero downtime
- Instant rollback
- Easy to test

**Cons:**
- 2x infrastructure cost
- Data drift between envs

**When to use:** Critical models where downtime is unacceptable

## Pattern 2: Shadow Mode

New model runs alongside old model but doesn't impact decisions.

**How it works:**
1. Old model makes decision (used by users)
2. New model also runs in background (not used)
3. Compare outputs
4. When 98%+ agreement, cut over

**Pros:**
- Zero risk (new model never impacts users)
- High confidence cutover
- Real-world validation

**Cons:**
- 2x compute cost
- Longer time to deployment

**When to use:** High-stakes decisions (credit, medical)

## Pattern 3: Canary Release

Deploy to small % of users first, expand slowly.

**How it works:**
1. Deploy to 1% of users
2. Monitor accuracy/latency
3. If good, expand to 5%
4. Continue expanding to 100%

**Pros:**
- Catch issues early
- Minimize blast radius
- Good telemetry

**Cons:**
- Unequal treatment of users
- Slower rollout

**When to use:** Most production scenarios

## Pattern 4: A/B Testing

Run old and new model for randomly selected users.

**How it works:**
1. Randomly select 50% of users
2. Show them old model results
3. Other 50% see new model
4. Compare outcomes over time

**Pros:**
- Statistically rigorous
- Measures real business impact
- Fair comparison

**Cons:**
- Some users get worse experience
- Requires longer test period

**When to use:** When need business metrics not just accuracy

## Pattern 5: Gradual Rollout

Deploy once, monitor closely, roll back if needed.

**How it works:**
1. Deploy to production
2. Intensive monitoring (metrics, errors, performance)
3. If problems: instant rollback
4. If good: declare victory

**Pros:**
- Simplest to implement
- Most common in practice

**Cons:**
- Some customers see failures
- Requires fast rollback mechanism

**When to use:** Non-critical models, mature teams

## Rollback Procedures

Every deployment needs a rollback plan:

- [ ] Previous model version ready to re-deploy
- [ ] Data rollback procedure if needed
- [ ] Testing of rollback mechanism
- [ ] Clear trigger for rollback (when to do it)
- [ ] Team on standby when deploying

## Monitoring Requirements

Deploy only if you can monitor:
- [ ] Model accuracy (vs ground truth)
- [ ] Prediction latency
- [ ] Error rates
- [ ] Data drift detection
- [ ] Business metrics

Without monitoring, you're flying blind.

---

Choose deployment pattern based on risk tolerance and monitoring capability.
