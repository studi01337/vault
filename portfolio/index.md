---
title: Portfolio
alias: portfolio
plugins:
  toc: false
---

<!-- cards --><p data-card class="center grid-2"></p>
```dataviewjs
let pages = dv.pages('"portfolio"')

const root = {container: dv.el("ul", "")};

dv.array(Array.from(pages))
  .filter(p => p.file.name != "index")
  .sort(k => k.file.frontmatter.year, 'asc')
  .map(p => {
    const li = dv.el("li", "", root)
    const list = {container: dv.el("ul", "", {container: li}) };
    const fm = p.file.frontmatter
    dv.el("li", `<img src="${fm.logo}"></img>`, list);
    dv.el("li", `<h2 class="mb-0">${fm.name}</h2>`, list);
    dv.el("li", `<mark class="d-inline-block m-auto mb-4 px-2"><small>${fm.year} - ${fm.role}</small></mark>`, list);
    return dv.el("li", fm.text, list);
  })

```
<!-- end:cards --><p data-end></p>