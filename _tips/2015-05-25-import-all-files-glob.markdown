---
layout: tips
title: Python Import folder names

---

To import only folder names in the sub-directory use * after the path to the directory

```python
import glob
import os

names = [os.path.basename(x) for x in glob.glob('PATH_TO_SUBDIRECTORY/*')]

```
