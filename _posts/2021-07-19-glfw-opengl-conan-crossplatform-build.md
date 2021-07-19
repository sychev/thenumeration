---
title:  "GLFW + OpenGL + Conan crossplatform build"
mathjax: true
layout: post
categories: media
comments: true
---

With [Conan](https://conan.io/) it's easy to create simple crossplatform project for OpenGL with GLFW as windowing API. This first article still in production.


Here is example of one of the highlighting.

{% highlight powershell %}

RMDIR /Q /S build.win64
MKDIR build.win64
PUSHD build.win64

conan install ..
cmake .. -G "Visual Studio 16 2019"
MSBuild.exe -p:Configuration=MinSizeRel -p:BuildProjectReferences=false gameone.sln
.\bin\gameone.exe
cd ..

{% endhighlight %}

<!--
rougify list
-->