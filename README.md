x3270-xft
=========

x3270 terminal emulator currently uses old X11 core font system which disallows use of anti-aliased (smooth) fonts like .otf, .ttf and so forth. Switch to modern Xft (X FreeType, which supports anti-aliasing of fonts) font system is recommended for all X11 applications.

x3270.freetypeFont resource should be used to specify FreeType font name in [Xft format] (e.g. monospace-12):
```
<family>-<size>:<name>=<value>...
```
If you don't specify x3270.freetypeFont then x3270 acts as always.

This patch should be applied to 3.3.15ga4 version of x3270 using:
```sh
cd x3270-3.3 && patch -p1 <x3270.patch
```

[Xft format]:http://www.keithp.com/~keithp/render/Xft.tutorial
