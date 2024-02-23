---
title: Tips for Linux
categories: [Tool, Linux]
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
# Reference: 
