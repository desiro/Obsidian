start_time:: {{time:HH:mm}}
end_time::
break:: 
status:: 
Tags: #daily
Links: [[{{title}}]], [[TODO]]

---
# TODOs

### Due this week
```dataview
TASK
WHERE !completed AND !contains(tags, "#waiting")
  AND
  ( ( due AND
      date(due).weekyear <= date("{{date:YYYY-MM-DD}}").weekyear AND
      date(due).year <= date("{{date:YYYY-MM-DD}}").year)
    OR
    ( scheduled AND
      date(scheduled).year <= date("{{date:YYYY-MM-DD}}").year AND
      date(scheduled).weekyear <= date("{{date:YYYY-MM-DD}}").weekyear) )
SORT due
```
### Due this week (waiting)
```dataview
TASK
WHERE !completed AND due AND date(due).weekyear <= date("{{date:YYYY-MM-DD}}").weekyear AND date(due).year <= date("{{date:YYYY-MM-DD}}").year AND contains(tags, "#waiting")
```
### Other TODOs with no due date
```dataview
TASK
WHERE !completed AND !due
SORT scheduled
```
### Completed today
```dataview
TASK
WHERE completed AND completion = date("{{date:YYYY-MM-DD}}")
```

---
# Log




