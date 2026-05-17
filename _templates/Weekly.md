<%*
const title = tp.date.now("YYYY-[W]ww");
await tp.file.rename(title);
%>---
week: <% tp.date.now("YYYY-[W]ww") %>
tags: [weekly]
---

# Week <% tp.date.now("ww") %>, <% tp.date.now("YYYY") %>

## Intention this week



## Top 3 outcomes

- [ ] 
- [ ] 
- [ ] 

## Daily notes this week

```dataview
LIST
FROM "01 Daily"
WHERE file.cday >= date("<% tp.date.now("YYYY-MM-DD", -7) %>") AND file.cday <= date("<% tp.date.now("YYYY-MM-DD") %>")
SORT file.cday ASC
```

## Tasks completed this week

```dataview
TASK FROM ""
WHERE completed AND completion >= date("<% tp.date.now("YYYY-MM-DD", -7) %>")
SORT completion DESC
```

## Open tasks coming up

```dataview
TASK FROM ""
WHERE !completed AND due
SORT due ASC
LIMIT 20
```

## Review

- **What worked**: 
- **What didn't**: 
- **One thing to adjust next week**: 
