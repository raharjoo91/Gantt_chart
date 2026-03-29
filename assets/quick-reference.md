# Quick Reference: Google Sheets Formulas for Gantt Charts

## Duration Formula
```
=End Date Cell - Start Date Cell
```
Example: `=C2-B2`

## Conditional Formatting Formula (Grid Method)
```
=AND(Date Cell Header >= Start Date Cell, Date Cell Header <= End Date Cell)
```
Example: `=AND(F$1>=$B2, F$1<=$C2)`

### Formula Breakdown:
- `F$1` = The date in the header row (absolute reference for row)
- `$B2` = The start date for this task (absolute reference for column)
- `$C2` = The end date for this task (absolute reference for column)
- `AND()` = Checks if the header date falls within the task date range

## Date Increment Formula (for timeline header)
```
=Previous Cell + 1
```
Example: In cell G1: `=F1+1`

## Tips
- Use `$` to lock rows or columns when dragging formulas
- Format dates consistently: Select cells → Format → Number → Date
- To show weekdays only, use a more complex formula or manually skip weekends
