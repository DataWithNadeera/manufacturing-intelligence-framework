# First Pass Yield (FPY)

## Business Definition

First Pass Yield (FPY) measures the percentage of units that pass through a manufacturing process correctly the first time without requiring rework, repair, or correction.

FPY is one of the most important indicators of manufacturing quality and process effectiveness.

---

## Formula

FPY = Good Units Produced / Total Units Produced

---

## Required Data Fields

| Field                | Description                        |
| -------------------- | ---------------------------------- |
| Production Date      | Date of production                 |
| Total Units Produced | Total quantity manufactured        |
| Good Units Produced  | Units meeting quality requirements |
| Rejected Units       | Defective units                    |
| Reworked Units       | Units requiring correction         |

---

## Power BI DAX Measure

```DAX
FPY % =
DIVIDE(
    SUM('Production'[Good Units Produced]),
    SUM('Production'[Total Units Produced]),
    0
)
```

---

## Executive Value

A high FPY indicates:

* Stable production processes
* Lower rework costs
* Higher customer satisfaction
* Better manufacturing efficiency

A low FPY may indicate:

* Process variation
* Training issues
* Equipment problems
* Quality control weaknesses

---

## Manufacturing Example

Total Units Produced = 10,000

Good Units Produced = 9,500

FPY = 9,500 / 10,000

FPY = 95%

This means 95% of products passed quality requirements the first time without rework.

---

## Common Mistakes

* Including reworked units as first-pass successes
* Ignoring inspection failures
* Using shipped quantity instead of produced quantity
* Calculating FPY at an aggregated level without process-level analysis

---

## Recommended Visuals

* KPI Card
* Monthly Trend Line
* Production Line Comparison
* Factory Comparison
* Quality Heat Map
