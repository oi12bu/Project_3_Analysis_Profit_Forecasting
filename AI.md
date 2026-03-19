# AI Usage Documentation

> This document tracks all use of AI tools throughout the project lifecycle.   
> Each team member is responsible for keeping their section up to date.   
> **No judgment** — this document is for transparency and reproducibility, not evaluation.

---

## Table of Contents

- [AI USE: Bea](#AI-USE:-Bea)
- [AI USE: Elton](#AI-USE:-Elton)
- [AI USE: Kainen](#AI-USE:-Kainen)

---

## AI USE: Bea

**Name:** Bea Sauve   
**Role:** Project Manager   

### AI Tools Used

| Tool | Version/Model | Purpose |
|------|--------------|---------|
| Claude | Claude Sonnet 4.6 | Coding Assistance |

### Interactions Log

#### Entry 1 — `2026-03-16`

**Task:** Create a template for our AI.MD

**Prompt(s) Used:**
```
Can you design a template for an AI.md in python? This will be used to document any use of AI in the project and I need 3 sections, one  for each teammember.
```

**AI Output Summary:**
AI produced a template for this document with commented sections that gave examples of what could be written in each section.

**Code/Content Adopted:** Yes, This document was built off the template

**Files Affected:**
- `AI.MD`

**Notes:**
No Additional Notes

---

#### Entry 2 — `2026-03-14`

**Task:** Forecast production lines

**Prompt(s) Used:**
```
I provided AI with the analysis charts plotted for the productionline forecasting. I Asked it to describe the trends and seasonality per chart and what type of forecasting should be used based on the data protrayed. Post forecasting, I showed the AI my charts and asked it how the charts could be improved.
```

**AI Output Summary:**
AI produced a breakdown analysis of each chart explaining what the trends, seasonal, and remainder represented per chart. It pointed out models that may best fit each product line.
For the second prompt, AI pointed out that I should add a floor function to my model to so projections dont go into the negatives. It also pointed out the large confidence intervals and their significance

**Code/Content Adopted:** Yes, While code was not taken or suggested from the AI. I did analyze and implement the suggestions it provided.

**Files Affected:**
- `Project_3_Technical_Report`

**Notes:**
No Additional Notes

---

## AI USE: Elton

**Name:** Elton Nichols   
**Role:** Version Control Manager

### AI Tools Used

| Tool | Version/Model | Purpose |
|------|--------------|---------|
|    |    |   |

### Interactions Log

#### Entry 1 — `YYYY-MM-DD`

**Task:** <!-- What were you trying to accomplish? -->

**Prompt(s) Used:**
```
<!-- Paste the exact prompt(s) you sent to the AI -->
```

**AI Output Summary:**
<!-- Briefly describe what the AI produced -->

**Code/Content Adopted:** <!-- Yes / No / Partially -->

**Files Affected:**
- `<!-- path/to/file.py -->`

**Notes:**
<!-- Any observations, modifications made, or caveats about the AI output -->

---

<!-- Duplicate the entry block above for each additional AI interaction -->

---

## AI USE: Kainen

**Name:** Kainen Osborne   
**Role:** Analysis Auditor   

### AI Tools Used

| Tool | Version/Model | Purpose |
|------|--------------|---------|
| Claude | Claude Sonnet 4.6 | Coding Assistance |

### Interactions Log

#### Entry 1 — `2026-03-16`

**Task:** Fixing some bugs within my forecasting.

**Prompt(s) Used:**

**Prompt:** Some product lines show a flat forecast line instead of a shaped
seasonal forecast. Why, and how do I fix it?


**AI Output Summary:**
Claude explained that `auto.arima()` was selecting ARIMA(0,0,0) a plain mean model when the seasonal signal was too weak over
29 observations to justify extra parameters. The fix added an `arimaorder()` check to detect the flat model and override to STL, which always reattaches the seasonal component.

**Code/Content Adopted:** Yes

**Files Affected:**
Project_3_Production.Rmd

**Notes:**
No notes
---

<!-- Duplicate the entry block above for each additional AI interaction -->

---

