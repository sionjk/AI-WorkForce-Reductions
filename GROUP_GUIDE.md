# AI and workforce reductions | Group project guide

## The question we’re answering

**How did reported tech layoffs vary over time and across industries from 2020 to 2026, and what role, if any, did employers say AI played in the March 2026 cuts?**

Use all **2,470 layoff records** for the timeline and industry comparisons. Use the **18 records from March 2026** to examine what employers actually said about those cuts. March is the latest full calendar month in this file, and we can review every event in it. Our findings about employers’ explanations apply to that month.

## What’s already done

- [x] **The cleaning notebook runs from start to finish.** `COP 4283 Final Project.ipynb` loads the four source CSVs, checks for exact duplicates and missing values, and prepares each dataset separately. Its validation checks pass.
- [x] **The layoff table is ready for analysis.** The notebook cleans dates and category labels, converts workforce percentages and funding amounts to numbers, and adds year, month, AI-group, and missing-headcount fields. It preserves all 2,470 records, including 878 with unknown employee counts.
- [x] **Three summaries are ready.** The monthly and industry summaries each account for all 2,470 records. The headquarters-country summary covers 2,468 because two records have an unknown country. Each summary reports event counts, known employee cuts, and the number of events with a disclosed headcount.

**Getting started:** Extract `Final Project.zip` and run the notebook from top to bottom in the folder with the four original CSVs. That produces four cleaned CSVs and three summaries. Use **`layoffs_clean.csv`** whenever a chart combines month, industry, and country. Use `monthly_layoffs.csv`, `industry_layoffs.csv`, and `country_layoffs.csv` to check the corresponding totals.

## What each person can start next

### Daniel Schevis — Data handoff and source tracking

- Update the notebook’s opening research question to match this guide. Give Sion and Brody the cleaned event file and the three summaries so chart work can begin.
- Filter the cleaned event table to March 2026 and sort its 18 rows by date, then company. Give Carissa and Madison one shared review sheet with columns for company, event date, original source, verified link, speaker, short supporting passage, category, and reviewer. Keep a note if two records turn out to cover the same announcement.

### Carissa Hudson — Employer explanations and evidence summary

- Review rows 1–9 of Daniel’s sorted March sheet. Find the employer’s explanation for each round and classify it using the rules below. Keep a row when the reason is unclear.
- Cross-check ambiguous cases with Madison. Give Brody the agreed counts, the number of distinct events reviewed, and one sourced example that illustrates the difference between AI taking over a task and a company redirecting spending toward AI, if the evidence supports one.

### Madison Simons — Full-period comparisons and March review

- Use the cleaned data to identify one change over time and one difference across industries. Give Sion the periods, industries, and event counts behind each observation. If comparing employees affected, include how many events disclosed headcounts.
- Review March rows 10–18 and reconcile uncertain classifications with Carissa. For the supporting company comparison, verify the workforce-percentage medians and sample sizes, then give Brody a sentence explaining what those figures measure.

### Sion King — Interactive timeline and presentation opening

- Start the Altair timeline from the cleaned event file while the March review is underway. Show monthly event counts across the full period, let readers compare industries and filter by headquarters country, and flag the partial first and last months. Check that the unfiltered event counts sum to 2,470.
- Open the presentation with the full-period question and one pattern verified with Madison. Then select March 2026 and hand off to Brody to show what an employer said about a specific round.

### Brody Reiter — March evidence view and presentation findings

- Set up the four-category evidence view while Carissa and Madison read the sources. Once they agree on the classifications, populate the bars from their review sheet. Selecting a bar should reveal the companies, supporting passages, and working links behind its count.
- Present one employer explanation and one case where the evidence is ambiguous, if available. Coordinate filters with Sion so both views show the same selected industry and headquarters country. Display the number of reviewed events in that selection.

## How to classify the March events

Look for a company statement, earnings call, or article that quotes or clearly attributes an explanation to management. All 17 March web addresses in the file contain spaces. The Zendesk row lists only “Internal memo.” Verify the company, date, and round of cuts before saving a working link. If a link cannot be recovered, search the company and announcement date.

Give each distinct event the **first applicable category** below. Keep additional reasons in the notes.

| Category | What qualifies |
| --- | --- |
| AI took over work | The employer explicitly says AI performed tasks people previously did or reduced the staffing needed for those tasks, and links that change to the cuts. Record the task if named. |
| Other AI connection | The employer links the cuts to an AI strategy, such as shifting investment toward AI, without saying AI took over affected employees’ work. |
| Other stated reason | The employer gives a reason such as weaker demand, a merger, or closure and makes no explicit AI link to these cuts. Record the stated reason. |
| Reason unclear | The source is unavailable, gives no employer explanation, or offers only speculation. Record which applies. |

Count each event once, including unclear cases in the denominator. Even an explicit statement about AI taking over work does not establish how many individual jobs it replaced.

## How to read the data

- **Source and coverage.** The Kaggle package’s README, dated May 13, 2026, attributes the layoff data to a historical CSV and a Layoffs.fyi scrape, with a historical fallback. Our event file runs from March 13, 2020 through April 16, 2026. The tracker covers reported or otherwise verified tech layoffs. [Layoffs.fyi’s collection notes](https://layoffs.fyi/press/)
- **Company label.** The README defines `is_ai_company = True` as AI-, machine-learning-, or data-focused. A `False` value means the dataset did not flag the company as having that focus. The exact tagging rule is undocumented, and Clearbit appears with both values. Use the label for a descriptive comparison. Use employer statements to classify reasons.
- **Size and geography.** Of 2,470 records, 1,592 disclose an employee count and 1,534 disclose a workforce percentage. Keep events with unknown headcounts in frequency charts. Label totals of disclosed cuts accordingly. The country field identifies company headquarters, which can differ from where affected employees worked.
- **Supporting comparison.** In the original file, the median workforce cut among events disclosing a percentage was 18% for flagged records (202 events) and 19% for unflagged records (1,332 events). Verify those figures in the cleaned file before presenting them. The U.S. labor, global labor, and news sentiment files are available for background if needed.

## Before we present

- [ ] The notebook opens with the agreed question. The dashboard opens on the full timeline and can jump to March or reset to all dates.
- [ ] The timeline and industry counts reconcile to the cleaned file. Empty filter combinations show “No recorded events for this selection.”
- [ ] Every March record is accounted for. The four category counts sum to the distinct events reviewed, and each classified explanation has a source.
- [ ] Sion and Brody can trace one full-period observation to the cleaned table and one March finding to an employer statement. Months outside March are labeled “Outside the source review.”
