Public Health Project Management: GitHub Repository Guidelines
Project Title: Gantt Chart Creation using Google Spreadsheets for Undergraduate Public Health Students
Target Audience: Public Health Undergraduate Students
Primary Tool: Google Sheets (with Excel context)

This document outlines the rules and standards for developing the GitHub educational repository. It ensures consistency, pedagogical value, and technical accuracy for students learning project management.

1. Technical Standards: Google Sheets Implementation
Since Google Sheets lacks a native "Gantt Chart" button, the repository must strictly teach one or both of the following methods.

Rule 1.1: The Standardized Data Structure
All tutorials and sample datasets must adhere to this specific column layout to ensure compatibility with instructions:

Column A
Column B
Column C
Column D
Task Name	Start Date	End Date	Duration (Days)

Note: Duration can be calculated using the formula =C2-B2.

Rule 1.2: The "Stacked Bar" Method (Chart-Based)
When teaching the chart-based approach (similar to Excel), the following steps must be explicitly documented:

Data Selection: Select Task Name, Start Date, and Duration.
Chart Type: Insert a Stacked Bar Chart.
Series Configuration:
Set "Start Date" as the first series (Format to be White/Invisible with no border).
Set "Duration" as the second series (Format with a distinct color).
Axis Formatting: The vertical axis must be reversed so Task 1 appears at the top.
Rule 1.3: The "Conditional Formatting" Method (Grid-Based)
When teaching the grid-based approach (manual timeline), the following logic is required:

Timeline Header: Create a row of dates (daily or weekly) across the top columns.
Formula Logic: Use a formula (e.g., =AND(F$1>=$B2, F$1<=$C2)) to check if a cell falls within the Start/End range.
Visualization: Apply Conditional Formatting to change cell fill color based on the formula result (TRUE).
2. GitHub Repository Structure
The repository must be organized into a modular, weekly progression. Each week requires a dedicated directory containing specific assets.

Rule 2.1: Folder Structure
The root directory must follow this naming convention:

text

/public-health-gantt-course
├── week-01-basics-planning/
├── week-02-excel-fundamentals/
├── week-03-google-sheets-gantt/
└── week-04-culminating-project/
Rule 2.2: Weekly Content Requirements
Every weekly folder must contain:

README.md: The primary instruction sheet (step-by-step lab style).
/assets: Folder containing screenshots, sample CSVs, or template links.
/examples: A completed sample of what the student should achieve by the end of the week.
Rule 2.3: Weekly Progression Logic
Week 01: Concepts of project planning in Public Health (e.g., outbreak response timeline, study design phases). No complex tools yet.
Week 02: Excel method (Stacked Bar). Use this to bridge the gap for students familiar with Excel, then transition to Sheets.
Week 03: Google Sheets method. Focus on the "Conditional Formatting" approach for customization or the "Stacked Bar" method for visualization.
Week 04: Final assignment.
3. Pedagogical Guidelines for Public Health Context
Rule 3.1: Relevance of Examples
All dummy data used in tutorials must be relevant to Public Health.

Acceptable Examples: Planning a vaccination drive, timeline for a cohort study, organizing a community health seminar, grant application milestones.
Unacceptable Examples: Software development sprints, construction timelines, marketing campaigns.
Rule 3.2: Collaborative Focus
Since Google Sheets is a collaborative tool, at least one exercise in Week 03 must require:

Sharing a sheet with a peer.
Adding comments to specific tasks (simulating team feedback).
Tracking revision history.
Rule 3.3: Template Usage
While teaching from scratch is required, the repository must also provide a curated list of "Ready-Made" templates in the assets folder for reference.

Allowed Sources: Unito, TeamGantt, or a custom template pre-loaded by the instructor.
Instruction: Students must be able to explain how the template works (formulas used), not just fill it in.
4. Assessment and Rubrics
Rule 4.1: The Final Project (Week 04)
Students must create a Gantt chart for a self-selected Public Health project.

Requirement: It must include at least 10 tasks.
Requirement: It must show 3 distinct phases (e.g., Planning, Implementation, Evaluation).
Requirement: It must utilize color-coding to distinguish task types.
Rule 4.2: Self-Check Checklist
Every README.md must end with a self-check rubric. Example criteria:

 Does the vertical axis list tasks in the correct order?
 Is the "Start Date" bar invisible/white?
 Do the task durations accurately reflect the data?
 Have dependencies (where one task must finish before another starts) been visually represented?
5. File Formatting Standards
Rule 5.1: Markdown Syntax
Use H2 (##) for main steps.
Use bold for UI elements (e.g., Click Insert, select Chart).
Use code blocks for formulas (e.g., =B2+C2).
Rule 5.2: Image Standards
Screenshots must be cropped to the relevant action area.
Images must be stored in /assets/images within the respective week's folder.
Alt-text must be provided for accessibility.
Rule 5.3: File Extensions
Google Sheets files should be shared as "Anyone with the link can view" and provided as .gsheet links or CSV exports if version control is needed.
Do not upload binary Excel files (.xlsx) as the primary source for Google Sheets weeks; use them only for cross-reference in Week 02.