---
layout: tips
title: Bash copy folder names

---

Copy folder names into a new directory without copying elements.

rsync -a --include='*/' --exclude='*' /some/path/dir/ dir
