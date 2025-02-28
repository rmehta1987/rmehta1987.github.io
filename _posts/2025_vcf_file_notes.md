---
layout: post
title: Set of notes for manipulating VCF/BIM files.
---

Skip comments (starting with #) in VCF header using awk
awk '/^ *#/ {next}1' gnomad.genomes.v4.1.local_ancestry.afr.vcf 
