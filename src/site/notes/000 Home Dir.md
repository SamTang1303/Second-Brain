---
{"dg-publish":true,"permalink":"/000-home-dir/","tags":["type/meta","gardenEntry"],"dgHomeLink":true,"dgPassFrontmatter":false,"dgShowBacklinks":false,"dgShowLocalGraph":false,"dgShowInlineTitle":false}
---

# 000 Home Dir

1. **[[010 Academics|010 Academics]]↓**
2. **[[020 Improvements|020 Improvements]]↓**
3. **[[030 Faith|030 Faith]]↓**
4. **[[040 Self|040 Self]]↓**
5. **[[050 Obsidian|050 Obsidian]]↓**
6. **[[060 Thinking|060 Thinking]]↓**

> [!dataview] Recently Edited Notes
> ```dataview
> TABLE string(regexreplace(filter(file.etags, (x) => contains(x, "type")), "(?<=#).+(?=/)/", "")) as Type,
> string(regexreplace(filter(file.etags, (x) => contains(x, "bin")), "(?<=#).+(?=/)/", "")) as Topic
> FROM "/"
> SORT file.mtime DESC
> LIMIT 10

## Utilities
| [[Inbox|📩]]  |  [[Black Hole|🔭]]  |  [[Scratch Note|🗒]]  |  [[Media Hub|🎥]]  |  [[Mobile Scratch Note|📱]] |

## To-Do
