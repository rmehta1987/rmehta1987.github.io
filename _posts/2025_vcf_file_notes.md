---
layout: post
title: Set of notes for manipulating VCF/BIM files.
---

Skip comments (starting with #) in VCF header using awk
awk '/^ *#/ {next}1' file.vcf 

Find the interesection of two columns within two text files, awk arrays are dictionaries so makes it easy
$ awk 'BEGIN { FS = "\t" } NR==FNR { col12[$1"\t"$2]=$1"-"$2"-"$3"-"$4 } NR!=FNR { if ($1"\t"$2 in col12) print $1"-"$2"-"$3"-"$4"\t"col12[$1"\t"$2]}' file1.vcf file2.txt > file2_intersects_with_file1.txt
