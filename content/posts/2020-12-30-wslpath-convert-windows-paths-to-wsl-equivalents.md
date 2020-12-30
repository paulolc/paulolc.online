---
template: post
title: 'wslpath - convert windows paths to wsl equivalents '
slug: wslpath
draft: false
date: 2020-12-30T13:23:36.509Z
description: >-
  If working in WSL and need to convert a windows path to POSIX (Linux, WSL).
  Use wslpath. 
category: tips
---
WSL is embeded in my workflow alongside my IDEs VS Code, Intellij IDEA and windows explorer. I use it for everything. From launching programs to search for strings in code or documents.

Many times I'm browsing the filesystem through my work directories and in one specific directory I want to search files from there. Usually I use the find command, but I have to convert the windows path I have in windows explorer to its WSL counterpart which is different. So, tipically I do it by hand. I replace the 'C:\' with '/mnt/c' and replace the backward slashes ('\') with forward ones ('/')  as posix dictates it. This is cumbersome and for long it bothered me. 

Finally I took the time to search for a tool to do it and there it was: **wslpath**

```
$ wslpath "C:\Windows\system32"/mnt/c/Windows/system
```





Wonderful.
