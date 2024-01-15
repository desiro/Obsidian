
---
# TODOs

## Completed this week
```dataview
TASK
WHERE completed AND date(completion).weekyear = date("{{date:YYYY-MM-DD}}").weekyear AND date(due).year = date("{{date:YYYY-MM-DD}}").year
FLATTEN tags
GROUP BY tags
```

---
# Log


