---
layout: post
title: Python Reading File Notes

---

Since analyzing genetic data also requires reading in lots of text type of files and I always forget how to do read files in python as well process the text.  So I'm leaving this post for all tricks and tips for reading in files for Matlab and Python.

This will return a list of the elements in text while removing all new lines.

file = open("pythongene.txt",r').read().splitlines()

Example:

If text is:
ABCD

EFGH

JKL

file is a list containing ['ABCD,'EFGH','JKL']
