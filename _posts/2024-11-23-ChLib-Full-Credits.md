---
layout: post
title: ChLib Full Credits
date: 2024-11-23 00:00
description: Full references for my ChLib
tags: ChLib
categories: ChLib
related_posts: true
toc:
  beginning: true
---

These are the credits of papers, source code, and websites, which help me write my library codes.



## Data Structure

##### Binary Search Tree

* Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest, and Clifford Stein. 2009. Introduction to Algorithms, Third Edition (3rd. ed.). The MIT Press.



##### AVL Tree

* Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest, and Clifford Stein. 2009. Introduction to Algorithms, Third Edition (3rd. ed.). The MIT Press.



## String

##### UTF-8 based String

* http://utf8everywhere.org/



## Memory Allocator

##### Dynamic Block Allocator

* `idBlockAlloc` from idSoftware Doom 3 : https://github.com/id-Software/DOOM-3/blob/a9c49da5afb18201d31e3f0a429a037e56ce2b9a/neo/idlib/Heap.h
  * GPL-3.0 license




### Arena Allocator

* Arena Allocator by Ryan Fleury : https://www.rfleury.com/p/untangling-lifetimes-the-arena-allocator



### Buddy Allocator

* Buddy Allcoator by gingerBill : https://www.gingerbill.org/article/2021/12/02/memory-allocation-strategies-006/#fnref:5



## HashMap

* Robin Hood Hasing by Pedro Celis : https://cs.uwaterloo.ca/research/tr/1986/CS-86-14.pdf
* Robin Hood Hash Map
  * Very Fast HashMap in C++ by Martin Leitner-Ankerl (Part 1) : https://martin.ankerl.com/2016/09/15/very-fast-hashmap-in-c-part-1/
  * Very Fast HashMap in C++ by Martin Leitner-Ankerl (Part 2) : https://martin.ankerl.com/2016/09/21/very-fast-hashmap-in-c-part-2/
  * Very Fast HashMap in C++ by Martin Leitner-Ankerl (Part 3) : https://martin.ankerl.com/2016/09/21/very-fast-hashmap-in-c-part-3/
* Robin HOOD Hash Map C Implementation by rmind : https://github.com/rmind/rhashmap
  * [BSD-2 Clause License](###BSD-2 Clause License)

* Robin Hood optimized unordered hashmap by Martin Leitner-Ankerl : https://github.com/martinus/unordered_dense/blob/main/include/ankerl/unordered_dense.h 
  * MIT License



## Window

##### ChWindow for windows, android, linux, mac, and so on

* ChWindow library copies the win32 part of the glfw first.
* GLFW : https://www.glfw.org/
* SDL : https://www.libsdl.org/



## Math

##### Conjugate Gradient Method

* Nocedal, J., & Wright, S. J. (2006). *Numerical optimization* (2nd ed.). Springer. 



##### Cholesky Decomposition

* Davis, T., Rajamanickam, S., & Sid-Lakhdar, W. (2016). A survey of direct methods for sparse linear systems. *Acta Numerica,* *25*, 383-566. doi:10.1017/S0962492916000076
* Ruschel, João Paulo Tarasconi, Bachelor degree, "Parallel Implementations of the Cholesky Decomposition on CPUs and GPUs" Universidade Federal Do Rio Grande Do Sul, Instituto De Informatica, 2016, pp. 29-30.



## Random

##### Permuted Congruential Generator

* https://www.pcg-random.org/
* https://github.com/imneme/pcg-c-basic
* https://github.com/imneme/pcg-c
* https://en.wikipedia.org/wiki/Permuted_congruential_generator



##### Uniform Random Float

* http://mumble.net/~campbell/2014/04/28/uniform-random-float
* https://mumble.net/~campbell/2014/04/28/random_real.c



## Language

##### Lexer and Parser

* Compiler Tutorial : https://github.com/DoctorWkt/acwj
  * GNU General Public License v3.0




##### Parsing floating-point value

* [fast_float by Daniel Lemire](https://github.com/fastfloat/fast_float) by MIT License.

  * Daniel Lemire, [Number Parsing at a Gigabyte per Second](https://arxiv.org/abs/2101.11408), Software: Practice and Experience 51 (8), 2021.

  * Noble Mushtak, Daniel Lemire, [Fast Number Parsing Without Fallback](https://arxiv.org/abs/2212.06644), Software: Practice and Experience 53 (7), 2023.

* https://www.exploringbinary.com/how-strtod-works-and-sometimes-doesnt/

  How strtod() WOrks (and Sometimes Doesn't) 

  This is the work of extensive exploration on strtod() by Rick Regan.

* Emscripten : https://chromium.googlesource.com/external/github.com/kripken/emscripten/+/refs/tags/1.2.9/system/lib/libc/stdlib/strtod.c

  * MIT license
  * University of Illinois/NCSA Open Source License

  



## OpenGL

#### OpenGL Loader

* glad : https://github.com/Dav1dde/glad
  * glad : MIT License
  * Khronos Specification : Apache License Version 2.0
  * EGL Speification and Various headers



## Vulkan

### Vulkan Presentation System

* krOoze's Hello Triangle Tutorial : https://github.com/krOoze/Hello_Triangle
  * Unlicense (Permissions : Private use/Commercial Use/Modification/Distribution)



### Vulkan Loader

* volk : https://github.com/zeux/volk
  * MIT License



## File Formats

### PNG

* PNG Specification New : https://www.w3.org/TR/png-3/
* PNG Specification Old : http://libpng.org/pub/png/spec/1.2/PNG-Contents.html
* ZLIB Compressed Data Format Specification 3.3 : https://www.rfc-editor.org/rfc/rfc1950
* Deflate Compressed Data Format Specification 1.3 : https://www.rfc-editor.org/rfc/rfc1951
* PNG Parser : stb_image.h from https://github.com/nothings/stb of Sean Barrett
  * Public Domain or MIT open source license
* Zip Files: History, Explanation and Implementation by  https://www.hanshq.net/zip.html#huffman
* ZLIB Deflate Algorithm Explanation : https://www.zlib.net/feldspar.html
* PNG Parser Review : https://handmade.network/forums/articles/t/2363-implementing_a_basic_png_reader_the_handmade_way
* A. Moffat and A. Turpin, "On the implementation of minimum redundancy prefix codes," in IEEE Transactions on Communications, vol. 45, no. 10, pp. 1200-1207, Oct. 1997, doi: 10.1109/26.634683.
* Handmade Hero PNG Decoder Parts: https://handmadehero.org/



### Font

* OpenType Specification Version 1.9 : https://learn.microsoft.com/en-us/typography/opentype/spec/
* TrueType Reference Manual : https://developer.apple.com/fonts/TrueType-Reference-Manual/
* Handmade Hero Fonts Parts: https://handmadehero.org/
* Handmade Network Tutorial :
  * https://handmade.network/forums/articles/t/7330-implementing_a_font_reader_and_rasterizer_from_scratch%252C_part_1__ttf_font_reader.
  * https://handmade.network/forums/wip/t/7610-reading_ttf_files_and_rasterizing_them_using_a_handmade_approach%252C_part_2__rasterization
* Fonts and Layout for Global Scripts by Simon Coznes : https://simoncozens.github.io/fonts-and-layout//
  * How OpenType Works : https://simoncozens.github.io/fonts-and-layout/opentype.html
  * Introduction to OpenType Programming : https://simoncozens.github.io/fonts-and-layout/features.html
* FreeType : https://freetype.org/index.html
  * FreeType License (FTL) : https://gitlab.freedesktop.org/freetype/freetype/-/blob/master/docs/FTL.TXT
  * GPLv2 License : https://gitlab.freedesktop.org/freetype/freetype/-/blob/master/docs/GPLv2.TXT
* stb_truetype.h : https://github.com/nothings/stb/blob/master/stb_truetype.h
* How the stb_truetype Anti-Aliased Software Rasterizer v2 Works : https://www.nothings.org/gamedev/rasterize/
* Texts Rasterization Exposures : https://web.archive.org/web/20190329134110/http://www.antigrain.com/research/font_rasterization/
* Creating a Pixel Font from scratch by Cal Henderson : https://www.iamcal.com/misc/fonts/pixfonttut/
* Adaptive Subdivision of Bezier Curves : https://web.archive.org/web/20190329074058/http://antigrain.com:80/research/adaptive_bezier/index.html




### BMP

* BMP file format from Wikipedia : https://en.wikipedia.org/wiki/BMP_file_format
* MSND Device Independent Bitmap (DIB) : https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps
* MSDN BITMAPINFOHEADER structure : https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader?redirectedfrom=MSDN
* MSDN Windows Meta File Format Specification : https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2
* MSDN DeviceIndependentBitmap (DIB) format : https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/7376542a-cce9-4625-8ead-585e9538f9f1
* MSND BitCount Enumeration : https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/792153f4-1e99-4ec8-93cf-d171a5f33903
* Type of Bitmaps : https://learn.microsoft.com/en-us/windows/win32/gdiplus/-gdiplus-types-of-bitmaps-about



### OBJ

* https://aras-p.info/blog/2022/05/12/speeding-up-blender-obj-import/
* https://aras-p.info/blog/2022/05/14/comparing-obj-parse-libraries/
* https://github.com/guybrush77/rapidobj
  * MIT license

* https://github.com/blender/blender




## GUI

### IMGUI

* Immediate-Mode Graphics User Interfaces by Casey Muratori : https://caseymuratori.com/blog_0001
* UI rendering using Primitive Buffers : https://ruby0x1.github.io/machinery_blog_archive/post/ui-rendering-using-primitive-buffers/
* One Draw Call UI by Our Machinery : https://ruby0x1.github.io/machinery_blog_archive/post/one-draw-call-ui/index.html (The engine shutdowns. And people have archived their resources).
* imgui : https://github.com/ocornut/imgui/tree/master
  * MIT License

* Immediate Mode Graphical User Interfaces by Rickard Gustafsson and Johannes Algelind : https://www.cse.chalmers.se/edu/year/2011/course/TDA361/Advanced%20Computer%20Graphics/IMGUI.pdf

* Writing tools faster by Niklas Gray (Our Machinery) in GDC 2020 presentation.



## Hash

### CRC

* CRC Implementation : https://en.wikipedia.org/wiki/Computation_of_cyclic_redundancy_checks
* Sunshine's Homepage : http://www.sunshine2k.de/articles/coding/crc/understanding_crc.html
* CRC RevEng : https://reveng.sourceforge.io/crc-catalogue/
* CRC-64/ECMA-182 : https://www.ecma-international.org/wp-content/uploads/ECMA-182_1st_edition_december_1992.pdf
* CRC-32/CKSUM : https://pubs.opengroup.org/onlinepubs/7990989775/xcu/cksum.html
* CRC-16/IBM-3740
* CRC-8/GSM-A



### Martin Leitner-Ankerl Hash

* https://github.com/martinus/unordered_dense/blob/main/include/ankerl/unordered_dense.h 
  * MIT License
  * It's a stripped-down implementation of wyhash : https://github.com/wangyi-fudan/wyhash

### wyhash

* https://github.com/wangyi-fudan/wyhash
  * Unlicense



## Spline

* A Blossoming Development of Splines by Stephen Mann (2006).



## Rendering

### Scanline Fill

* How the stb_truetype Anti-Aliasdd Software Rasterizer Works : https://www.nothings.org/gamedev/rasterize/
* non-zero fill algorithm on wikipedia. : https://en.wikipedia.org/wiki/Nonzero-rule
* Chris Hecker series on perspective texture mapping : https://chrishecker.com/Miscellaneous_Technical_Articles



### Triangle Rasterization

* Triangle rasterization in practice by Fabian “ryg” Giesen : https://fgiesen.wordpress.com/2013/02/08/triangle-rasterization-in-practice/
* Optimizing the basic rasterizer by Fabian “ryg” Giesen : https://fgiesen.wordpress.com/2013/02/10/optimizing-the-basic-rasterizer/



### Terrain

* Tessellated Terrain Rendering with Dynamic LOD by victorbush : https://victorbush.com/2015/01/tessellated-terrain/



### Physically-Based Rendering

* Burley, B., & Studios, W. D. A. (2012, August). Physically-based shading at disney. In *Acm Siggraph* (Vol. 2012, pp. 1-7). vol. 2012.
  * https://disneyanimation.com/publications/physically-based-shading-at-disney/
  * https://github.com/wdas/brdf
* Physically Based Rendering in Filament
  * https://google.github.io/filament/Filament.html



## Model Data

* Models downloaded from Morgan McGuire's [Computer Graphics Archive](https://casual-effects.com/data)
  * Sibenik Cathedral
