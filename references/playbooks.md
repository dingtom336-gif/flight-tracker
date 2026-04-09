# Playbooks — flight-tracker

> CLI command sequences. Knowledge is for parameter mapping — never answer without executing.

---

## Playbook A: 7-Day Trend

**Trigger:** "price trend this week"

```bash
flyai search-flight --origin "{o}" --destination "{d}" --dep-date-start {today} --dep-date-end {today+7} --sort-type 3
```

**Output emphasis:** Show daily lowest as trend table.

---

## Playbook B: Advance Booking Compare

**Trigger:** "book now or wait?"

```bash
flyai search-flight --origin "{o}" --destination "{d}" --dep-date {target} --sort-type 3
# Compare with historical patterns from knowledge
```

**Output emphasis:** Show current price + booking window advice.

---

## Playbook C: Best Day in Month

**Trigger:** "cheapest day in June"

```bash
flyai search-flight --origin "{o}" --destination "{d}" --dep-date-start {month_start} --dep-date-end {month_end} --sort-type 3
```

**Output emphasis:** Full month scan, highlight cheapest day/week.

---

