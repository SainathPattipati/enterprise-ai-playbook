# Data Quality Framework for AI

## The Harsh Reality

You'll spend 80% of project time on data. This framework helps you manage it.

## Six Dimensions of AI Data Quality

### 1. Completeness
**How much data do you have?**
- Target: >95% values present
- Missing data is common and often systematic (not random)
- Mechanisms: mechanical failure, human error, system crash

**Checklist:**
- [ ] Identified all missing data
- [ ] Understood WHY it's missing
- [ ] Documented imputation strategy

### 2. Accuracy
**Is the data correct?**
- Target: >99% values correct
- Harder to measure than completeness
- Systematic errors are worse than random errors

**Checklist:**
- [ ] Validated sample of data manually
- [ ] Compared against alternative sources
- [ ] Documented known inaccuracies

### 3. Consistency
**Does the same thing mean the same thing everywhere?**
- Equipment IDs format changes across systems
- Date formats differ
- Unit conversions wrong

**Checklist:**
- [ ] Standardized all key fields
- [ ] Documentation of mappings
- [ ] Consistent units throughout

### 4. Timeliness
**Is data fresh enough?**
- Real-time data needs millisecond latency
- Monthly reporting can tolerate days of lag
- Age of data impacts model accuracy

**Checklist:**
- [ ] Documented data collection frequency
- [ ] Understood latency in data pipeline
- [ ] Models retrained at appropriate intervals

### 5. Validity
**Does data fit expected ranges?**
- Temperature readings > 100°C
- Negative inventory
- Missing required fields

**Checklist:**
- [ ] Defined valid ranges for each field
- [ ] Implemented validation rules
- [ ] Monitoring for violations

### 6. Uniqueness
**Are there duplicates?**
- Same transaction recorded twice
- Multiple systems with slightly different records
- Historical duplicates from mergers

**Checklist:**
- [ ] Identified duplicate detection method
- [ ] Understood data lineage
- [ ] Deduplication rules documented

## Assessment Checklist

For each key dataset:

- [ ] Documented data source and collection method
- [ ] Assessed completeness (% missing)
- [ ] Validated accuracy (spot check 100+ records)
- [ ] Checked consistency (values match other sources)
- [ ] Evaluated timeliness (how recent is data?)
- [ ] Defined valid ranges
- [ ] Identified duplicates

**Scoring:** 
- 0-20% issues = Good
- 21-50% issues = Needs work  
- 51%+ issues = Major cleanup required

## Remediation Roadmap

### Phase 1: Stabilization (Weeks 1-4)
- Stop hemorrhaging data (fix collection processes)
- Document what you have
- Implement basic validation

### Phase 2: Cleanup (Weeks 5-12)
- Fix identified issues
- Fill critical gaps
- Standardize formats

### Phase 3: Optimization (Weeks 13+)
- Optimize collection
- Automate validation
- Continuous monitoring

## Monitoring & Ongoing Governance

Set up monthly monitoring for:
- Missing data rate
- Validation failures
- Duplicate count
- Data freshness

**When to alert:** If any metric changes >10% from baseline

---

Good data quality is not one-time work. It's an ongoing commitment.
