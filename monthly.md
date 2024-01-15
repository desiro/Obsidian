```dataview
TABLE dateformat(date(file.name), "cccc") AS weekday, start_time AS start, end_time AS end, status
FROM "daily"
WHERE date(file.name).month = date(this.file.name).month AND date(file.name).year = date(this.file.name).year
SORT file.name
```
