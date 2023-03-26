---
title: Clean Bin and Obj Folders
author: Jaan
date: 2023-03-24 12:00:00 +0100
categories: [Blogging]
tags: [first]
---

# Easy script to clean all Bin and Obj folders
This small script will clean all Bin and Obj folders in your solution. Just copy it to your solution folder and run it.

```powershell
Get-ChildItem .\ -include bin,obj -Recurse | foreach ($_) { remove-item $_.fullname -Force -Recurse }
```