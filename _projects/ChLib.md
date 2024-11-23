---
layout: page
title: ChLib
description: My personal library
img: assets/img/chlib_background.png
importance: 1
category: work
related_publications: false
---

ChLib is my personal library that is used to build a game engine and other applications for my future plan. This library is built on top of these:

* C99
* [Unity Build](https://en.wikipedia.org/wiki/Unity_build)
* [4coder editor](https://4coder.net/)
* [raddebugger](https://github.com/EpicGamesExt/raddebugger)

, which helps me get fast build time and write codes pleasantly.



Here is the highlight list of my implementations ([Full credits here](/blog/2024/ChLib-Full-Credits)):

* ChSTL : All the data structures works with my allocators
  * BuddyBlock and Arena Allocator
  * Robin Hood Hash Map
  * Linear Algebra: Cholesky Decomposition, Conjugate Gradient.
* ChRender
  * Vulkan 1.3
* ChImage
  * PNG Decoder (+ ZLIB deflation)
  * BMP Decoder
* ChFontCook
  * OpenType/TrueType Font Decoder
  * Font Rasterizer
* ChGUI (Here are my [slides](/blog/2024/Building-GUI-from-scratch) for building this library)
  * Immediate Mode GUI
  * One draw call GUI rendering, inspired by Our Machinery
* ChModelData
  * Obj File Parser



Here are the pictures and gifs of my progresses:

* GUI: Button and Text Widget with overlapped multi windows.

  {% include figure.liquid loading="eager" path="assets/img/chgui_window_overlapping.gif" class="img-fluid rounded z-depth-1" zoomable=true %}

* Model Rendering

  {% include figure.liquid loading="eager" path="assets/img/chlib_background.png" class="img-fluid rounded z-depth-1" zoomable=true %}

