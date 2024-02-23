---
title: Tips for Linux
categories: [Tools, Linux]
tags: [diff]
---

# Basis
Compare two folders, 比較兩個目錄內檔案的差異，列出所有差異處
```
diff -bur folder1/ folder2/
```

比較兩個目錄內檔案的差異，只列出有差異的檔案名稱
```
diff -qr folder1/ folder2/
```
```
diff -qr folder1/ folder2/ | sort
```


# Handle files with patterns 
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


# Reference: 
