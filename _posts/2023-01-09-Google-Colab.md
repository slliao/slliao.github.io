---
title: Google Colab 
categories: [Tools, Python]
tags: [Google, Colab]
---

### Mount (unmount) Google Drive
```python
from google.colab import drive
drive.mount('/content/drive')
```
``` python
drive.mount('/drive', force_remount=True)
```
