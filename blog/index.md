---
title: The Blog
tags: blog/index
---

# The Blog

```dataview
table without id date, link(file.link, title) as title
from "blog" and -"blog/draft"
where file.link != [[blog/index]] 
and file.link != [[blog/dirrc]]
sort date desc
```