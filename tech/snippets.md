---
date: 2023-01-10
title: Snippets
tags: snippet
---
# Snippets

```js
const els = dom.querySelectorAll('[class]:not([class=""])')
for (const el of els){
    if(!["PRE", "UL"].includes(el.nodeName)) el.removeAttribute('class')
}
```

## dvjs

```dataviewjs
const pages = await dv.query(`table name, logo, role, text from "notes/portfolio"
where file.link != [[notes/portfolio/index]]`)
const c = this.container


pages.value.values.forEach(async (p, i) => {
	let div = await c.createEl("div", { cls: "d-flex flex-column flex-md-row mb-5" });
	let left = await div.createEl('div', { cls: "text-center" })
	left.insertAdjacentHTML('beforeend', `<img class="img-fluid rounded mb-5" src="${p[2]}" style="max-width: 200px;"></img>`);
	
	let innerdiv = await div.createEl('div', { cls: "px-4 overflow-auto" })
	innerdiv.createEl('p', { cls: "fw-bold d-block mb-4", text: `${p[1]} - ${p[3]}`})
	innerdiv.createEl('p', { cls: "small br", text: `${p[4]}`})
});
```