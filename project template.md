{{date:YYYY-MM-DD}} {{time:HH:mm}}
Tags: #project
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
WHERE completed AND (contains(text, "{{title}}") OR contains(tag, "#xxx"))
SORT due
```
### Meetings
```dataview
TASK
FROM "daily"
WHERE (contains(text, "{{title}}") OR contains(tags, "#xxx")) AND contains(tags, "#meeting")
SORT scheduled
```

---
# Notes


---
# References

[{{title}} Docs](P:\Documents\Projects\{{title}})
[{{title}} LINK](https://)