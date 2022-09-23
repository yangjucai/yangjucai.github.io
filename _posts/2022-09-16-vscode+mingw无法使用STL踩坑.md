---
layout: post
title: vscode+mingw无法使用STL
categories: [杂谈]
description: vscode+mingw无法使用STL踩坑实记
keywords: vscode, mingw, STL
---

<h1 align = "center">vscode+mingw无法使用STL踩坑实记</h1>

在vscode中使用mingw的c/c++环境时出现了无法使用STL的问题，gdb调试时出现

```c
During startup program exited with code 0xc0000139 [duplicate]
```

错误，问题就是加载了错误的dll, 在编译参数上加

```
"-static-libgcc",
"-static-libstdc++",
```

就不用再担心dll的问题了。