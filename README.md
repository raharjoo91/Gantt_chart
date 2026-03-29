# Public Health Project Management: Gantt Chart using Google Sheets

> A practical guide for creating Gantt Charts for public health program planning

## Target Audience
Public Health Undergraduate Students

## What You Will Learn
Create a Gantt Chart in Google Sheets to visualize project timelines for public health programs. This guide uses a **TB Screening and School Nutrition Program to Prevent Stunting** as a practical example.

---

## Example Scenario: TB Screening & Nutrition Program at School

| Phase | Description |
|-------|-------------|
| **Planning** | Needs assessment, stakeholder coordination, resource preparation |
| **Implementation** | TB screening, nutrition education, stunting prevention training |
| **Evaluation** | Data analysis, report writing, follow-up planning |

---

## Method 1: Stacked Bar Chart (Recommended for Visual Timeline)

### Step 1: Prepare Your Data

Create a Google Sheet with these exact columns:

| | A | B | C | D |
|---|---|---|---|---|
| **1** | Task Name | Start Date | End Date | Duration (Days) |
| **2** | Stakeholder Meeting | 2025-04-01 | 2025-04-02 | `=C2-B2` |
| **3** | School Permission | 2025-04-03 | 2025-04-07 | `=C3-B3` |
| **4** | Volunteer Recruitment | 2025-04-05 | 2025-04-12 | `=C4-B4` |
| **5** | Training Health Workers | 2025-04-10 | 2025-04-15 | `=C5-B5` |
| **6** | TB Screening Day 1 | 2025-04-16 | 2025-04-16 | `=C6-B6` |
| **7** | TB Screening Day 2 | 2025-04-17 | 2025-04-17 | `=C7-B7` |
| **8** | Nutrition Education Session | 2025-04-18 | 2025-04-19 | `=C8-B8` |
| **9** | Parent Meeting | 2025-04-20 | 2025-04-20 | `=C9-B9` |
| **10** | Data Entry & Analysis | 2025-04-21 | 2025-04-27 | `=C10-B10` |
| **11** | Report Writing | 2025-04-25 | 2025-04-30 | `=C11-B11` |
| **12** | Follow-up Planning | 2025-05-01 | 2025-05-05 | `=C12-B12` |

**Formula Note:** Duration is calculated as `=C2-B2` (End Date minus Start Date)

### Step 2: Create the Chart

1. **Select your data**: Highlight columns A, B, and D (Task Name, Start Date, Duration)
   - **Don't include** the End Date column

2. **Insert chart**:
   - Click **Insert** → **Chart**
   - Or use the toolbar: Click the **Chart icon**

3. **Setup the chart type**:
   - In the Chart Editor, under **Setup** tab
   - Change **Chart type** to **Stacked bar chart**

### Step 3: Configure the Series

1. Go to the **Customize** tab in the Chart Editor

2. Click **Series** dropdown

3. **For "Start Date" series** (make it invisible):
   - Select **Start Date** from the dropdown
   - Set **Fill color** to **White** (or transparent)
   - Set **Line opacity** to **0%**

4. **For "Duration" series** (the visible bars):
   - Select **Duration** from the dropdown
   - Set **Fill color** to a visible color (e.g., blue or green)
   - Optionally add a **Border color**

### Step 4: Reverse the Vertical Axis

1. In the **Customize** tab, click **Vertical axis**

2. Check the box: **Reverse axis order**

This ensures Task 1 appears at the top (not the bottom).

### Step 5: Format the Horizontal Axis (Timeline)

1. In the **Customize** tab, click **Horizontal axis**

2. Adjust the date format:
   - Select a readable format (e.g., "Apr 1" or "1 Apr")

---

## Method 2: Conditional Formatting (Grid-Based Timeline)

### Step 1: Create a Timeline Header

1. In cell **F1**, enter the start date: `2025-04-01`

2. In cell **G1**, enter: `=F1+1`

3. Drag G1 across to create daily dates through your project end date

### Step 2: Add the Formula

For each task row (starting from row 2), use this formula in cell F2:

```
=AND(F$1>=$B2, F$1<=$C2)
```

Then drag this formula:
- **Right** across all date columns
- **Down** for all task rows

### Step 3: Apply Conditional Formatting

1. Select the entire grid (from F2 to the last date column for all tasks)

2. Click **Format** → **Conditional formatting**

3. Set up the rule:
   - **Format cells if**: **Is true**
   - **Value or formula**: `=AND(F$1>=$B2, F$1<=$C2)`
   - **Formatting style**: Choose a fill color (e.g., green)

4. Click **Done**

---

## Final Result Checklist

After creating your Gantt Chart, verify:

- [ ] The vertical axis lists tasks in the correct order (Task 1 at top)
- [ ] The "Start Date" bar is invisible/white (Method 1)
- [ ] Task durations accurately reflect the data
- [ ] Dependencies are visually represented (overlapping or sequential tasks)
- [ ] The chart clearly shows the three phases: Planning, Implementation, Evaluation
- [ ] Dates are readable and properly formatted

---

## Public Health Examples for Practice

| Program Type | Sample Tasks |
|--------------|--------------|
| **Vaccination Drive** | Site preparation, staff training, community mobilization, vaccination days, adverse event monitoring |
| **Cohort Study** | Protocol development, ethical approval, recruitment, baseline data collection, follow-up visits, data analysis |
| **Health Seminar** | Topic selection, speaker invitation, venue booking, promotion, event execution, feedback collection |
| **Outbreak Response** | Case investigation, contact tracing, containment measures, community education, monitoring & evaluation |

---

## Templates & Resources

### Ready-Made Templates
- [TeamGantt Google Sheets Template](https://teamgantt.com/google-sheets-gantt-chart-template)
- [Unito Project Tracking Template](https://unito.io/blog/google-sheets-gantt-chart/)

### Important Note
While templates are helpful, ensure you understand:
- How the duration formula works (`=End Date - Start Date`)
- How to customize conditional formatting rules
- How to adjust the chart for different project timelines

---

## Tips for Public Health Students

1. **Break down activities** into specific, measurable tasks
2. **Include buffer time** for unexpected delays
3. **Use color coding** to distinguish:
   - Planning phase (e.g., blue)
   - Implementation phase (e.g., green)
   - Evaluation phase (e.g., orange)
4. **Consider dependencies** - which tasks must finish before others can start?
5. **Share your Gantt chart** with team members for collaborative planning

---

## License

This educational resource is created for Public Health students in Indonesia.

## Contributing

This is an open educational resource. Feel free to adapt examples for your specific public health context.
