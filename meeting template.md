{{date:YYYY-MM-DD}} {{time:HH:mm}}
Tags: #meeting #mgw
Links: [[{{title}}]], [[TODO]], [[ProjectTitle]]

---
# {{title}}
### TODOs
```dataview
TASK
FROM "daily"
WHERE !completed AND contains(tags, "#meeting") AND (contains(text, "ProjectTitle") OR contains(tags, "#xxx")) AND date(start) = date("{{date:YYYY-MM-DD}}")
SORT due
```
### Completed
```dataview
TASK
FROM "daily"
WHERE completed AND contains(tags, "#meeting") AND (contains(text, "ProjectTitle") OR contains(tags, "#xxx")) AND date(start) = date("{{date:YYYY-MM-DD}}")
SORT due
```

---
# Notes


---
# References

[{{title}} Docs](P:\Documents\Tasks\{{title}})
[{{title}} LINK](https://)