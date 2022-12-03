---
title: Search Files in Command Line
categories: [Tools, Linux]
tags: Linux
---
Search file/搜尋檔案 (Linux Tips)

找出大於Gigabyte 的資料夾：
```console
# du -h -d 1 /var | grep '[0-9]G\>'
sudo find / -type f -name "*deh*"

sudo find / -type f -iname "*deh*"   
```

iname 不區分大小寫

查詢檔案名稱 (不區分大小寫)

find /etc -iname 'Network'

指定只要搜尋「檔案」名稱

find /var/log -iname '*.log' -type f

指定只要搜尋「目錄」名稱

find /etc -iname 'apache2' -type d

   補充說明：可用的 –type 參數值如下

b      block (buffered) special

c      character (unbuffered) special

d      directory ( 一般目錄 )

p      named pipe (FIFO)

f      regular file ( 一般檔案 )

l      symbolic link

s      socket

D      door (Solaris)

找尋所有檔案大小大於 50MB 的檔案
find /var -type f -size +50M

   註1: 不加上 –name 參數即代表搜尋所有檔案

找尋所有檔案大小小於 50MB 的檔案

find /var -type f -size -50M

尋找超過 7 天沒有被存取或修改過的檔案 (判斷檔案存取時間)

find $HOME -type f -atime +7

尋找曾經在 7 天內被存取或修改過的檔案 (判斷檔案存取時間)

find $HOME -type f -atime -7

尋找超過 10 分鐘沒有被存取或修改過的檔案 (判斷檔案存取時間)

find $HOME -type f -amin +10

尋找曾經在 10 分鐘內被存取或修改過的檔案 (判斷檔案存取時間)

find $HOME -type f -amin -10

尋找檔案建立時間已超過 30 天的檔案

find $HOME -type f -ctime +30

尋找特定使用者的檔案 ( 以帳號名稱 tom 為例 )

find $HOME -type f -user tom

