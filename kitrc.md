---
# 📂 Vault

vault:
  kit_folder: /Users/louis/code/s1337/studi01337.github.io
  include: 
    - '^pkrc.md'
    - '^(kitrc|index|navbar).md$'
    - '^blog/'
    - '^ui/index'
  exclude: 
    - '^kit/'
    - '^templates/'
    - '^blog/draft'

# 🧰 Kit

kit:
  version: latest
  dirs: true

# 🖥️ Site

site:
  id: rec_ce9p0lgo1msk9l0pk7hg
  name: Studio1337
  description: Welcome to Studio1337
  url: https://studio1337.tech
  keyswords: markdown, publishing, bloging, blog, api doc


# 🔌 Plugins

plugins: 
  theme: true
  header: true
  bg: true
  darkmode: "dark"
  toc: true
  modal: true
  navbar: true
  search: false
  social: true
  ga: "@ga|id:G-LC3WH6SJE1"
  cards: true
  css: true

theme:
  radius: none
  layout: 
    mode: stacked
    width: 800px
  primary: "#e01c6f"
  font: Informative
  headings:
    font: Shizuru

header:
  logo: https://studio1337.tech/assets/logo.svg

navbar:
  ui: header.right

bg:
  url: https://images.unsplash.com/photo-1539035104074-dee66086b5e3?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjI0MX0&auto=format&fit=crop&w=2550&q=80
  parallax: true

css:
  logo-height: 2rem

---
# KITRC

KITRC stands for Kit **R**un **C**ommands.
It holds your app global configuration. 

Edit settings or add plugins, and export the file in your kit. If the file is valid frontmatter wise, you should see a `kitrc.json` at the root of your kit folder.

Check out https://publishkit.dev
