---
date: 2023-01-10
title: MongoDB notes
tags: mongo, db, regex
---

## v6.0.1

```bash
mongorestore --nsInclude 'mydb.*' ~/backup
# backup folder should contain the "mydb" export folder
```

## regex

email that don't contain the `+` sign
```js
{email: {$regex: /^((?!\+).)*@tld.com$/}}
```

email that don't contain the word `louis` on a specific tld.
```js
{email: {$regex: /^((?!louis).)*@tld.com$/}}
```
