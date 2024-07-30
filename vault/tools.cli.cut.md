---
id: rhm5kejf1kldqchjs7mcqpm
title: Cut
desc: ''
updated: 1722256656809
created: 1722256583803
---

## Check for duplicate according to a column

```bash
cut -f1 '/home/allardpm/git_repos/COMMONS/dataset-extractor-lotus/data/230106_frozen_metadata_for_mines.csv' | sort | uniq -d
```
This will return the duplicates in the first column of the file.

