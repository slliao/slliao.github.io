---
title: Handle files with patterns 
categories: [Tools, Linux]
tags: Linux
---

## We can recursively Remove the files with certain patterns recursively under a folder.

### Removes files with find-exec 
```bash
find . -type f -name '*.txt~' -exec rm -f {} \;
```

### Remove files with find and xargs
```bash
find . -name "*.bak" | xargs rm
```
An argument ‘rm’ was passed by the ‘xargs’ command. i

