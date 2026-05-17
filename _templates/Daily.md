<%*
const title = tp.date.now("YYYY-MM-DD");
await tp.file.rename(title);
%>---
date: <% tp.date.now("YYYY-MM-DD") %>
energy: 
mode: 
tags: [daily]
---

# <% tp.date.now("dddd, MMMM Do YYYY") %>

## Energy check

- Energy: **low / medium / OH BOI**
- Mode: **deep focus / shallow / admin / rest**
- Sleep hours: 

## Top 3 today

- [ ] 
- [ ] 
- [ ] 

## Notes



## What got done today

```dataview
TASK FROM ""
WHERE completed AND completion = date("<% tp.date.now("YYYY-MM-DD") %>")
SORT completion ASC
```

## Rolled over (open + due today or earlier)

```dataview
TASK FROM ""
WHERE !completed AND due AND due <= date("<% tp.date.now("YYYY-MM-DD") %>")
SORT due ASC
LIMIT 15
```

## Tomorrow

- [ ] 
