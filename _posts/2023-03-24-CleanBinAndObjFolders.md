---
title: Clean Bin and Obj Folders
author: Jan Madsen
date: 2023-03-24 12:00:00 +0100
categories: [Blogging]
tags: [powershell, script, build]
---

# Easy script to clean all Bin and Obj folders
If you are a dotnet developer like me you have have issue where you suspect something has gone wrong in your build and you want to clean up all bin and obj folder but you have multiple projects and you don't know what project that is messing up your solution.
Then this small script might help you it will clean all Bin and Obj folders in your solution. Just copy it to your solution folder and run it.

```powershell
Get-ChildItem .\ -include bin,obj -Recurse | foreach ($_) { remove-item $_.fullname -Force -Recurse }
```
