---
layout: post
title: USDZ Files
---

<a href='/assets/usd/cube.usdz' rel='usdz'>
<img src='/assets/usd/cube.jpeg' />
</a>

Apple announched at WWDC 2018 that they are going to support _usdz_ file format throughout the system. This is the first time a 3d file format is supported system wide. I think this is a very good opportunity for modelers to show of their talent that is guaranteed to be supported throughout the iOS ecosystem. I hope the support will be extended to macOS as well.

A usdz file is a zero compression, unencrypted zip archive. The [spec](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html) is available on Pixar's website. This is just a fancy way of saying that usdz file is a collection of files containing the mesh as well as related textures packed together in a way so that they are easily accessible to the viewer.

The easiest way to create a usdz file is by using the _usdz_converter_ tool available with XCode 10 beta. At minimum, you will need start with a _Wavefront Obj_ file. 

Here is a same obj representing a simple cube.

```
# cube.obj
#
  
v  -0.5  -0.5  -0.5
v  -0.5  -0.5   0.5
v  -0.5   0.5  -0.5
v  -0.5   0.5   0.5
v   0.5  -0.5  -0.5
v   0.5  -0.5   0.5
v   0.5   0.5  -0.5
v   0.5   0.5   0.5

vn  0.0  0.0  1.0
vn  0.0  0.0 -1.0
vn  0.0  1.0  0.0
vn  0.0 -1.0  0.0
vn  1.0  0.0  0.0
vn -1.0  0.0  0.0

vt 0.0      0.0
vt 0.25     0.0
vt 0.5      0.0
vt 0.0      0.25
vt 0.25     0.25
vt 0.5      0.25
vt 0.0      0.5
vt 0.25     0.5
vt 0.5      0.5
vt 0.0      0.75
vt 0.25     0.75
vt 0.5      0.75

g cube_box
f  1/4/4  5/5/4  6/2/4 
f  1/4/4  6/2/4  2/1/4 
f  3/5/3  8/3/3  7/6/3 
f  3/5/3  4/2/3  8/3/3 
f  1/5/2  7/7/2  5/8/2
f  1/5/2  3/8/2  7/7/2 
f  2/5/1  6/6/1  8/9/1 
f  2/5/1  8/9/1  4/8/1 
f  1/7/6  4/11/6  3/10/6 
f  1/7/6  2/8/6  4/11/6 
f  5/9/5  7/12/5  8/11/5 
f  5/9/5  8/11/5  6/8/5 

```