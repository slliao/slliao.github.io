---
title: Handle files with patterns 
categories: [Tools, Linux]
tags: Linux
---

## Remove the files with certain patterns recursively under a folder.

### Delete all files in a directory apart from all .zip and .odt files as follows, while displaying what is being done.
```bash
$ rm -v !(*.zip|*.odt)


```

### Remove files with find-exec 
```bash
find . -type f -name '*.txt~' -exec rm -f {} \;
```

### Remove files with find and xargs
```bash
find . -name "*.bak" | xargs rm
```
An argument ‘rm’ was passed by the ‘xargs’ command. i

