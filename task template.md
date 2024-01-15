{{date:YYYY-MM-DD}} {{time:HH:mm}}
Tags: #task
Links: [[{{title}}]], [[TODO]]

---
# {{title}}
### TODOs
```dataview
TASK
FROM "daily"
WHERE !completed AND (contains(text, "{{title}}") OR contains(tags, "#xxx"))
SORT due
```
### Completed
```dataview
TASK
FROM "daily"
WHERE completed AND (contains(text, "{{title}}") OR contains(tags, "#xxx"))
SORT due
```

---
# Notes


---
# References

[{{title}} Docs](P:\Documents\Tasks\{{title}})
[{{title}} LINK](https://)