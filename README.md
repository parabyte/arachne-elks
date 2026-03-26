# Arachne Web Browser

## Introduction

This is the new home of the Arachne Elks fork.
expect no progress here for at least a month or so. As i am working on my bios project.


I plan to drop video modes not supported by elks.

Will keep in vga as there is 8bit vga cards out there. 

Initial port of this code will not use ems until. 

When ems shows up in official elks tree, I plan on adding in ems to this port

expect all other targets to be removed from this port.



The Arachne core source code has been released as
open source (GPLv2) with version 1.73 in 2003.

The LOPIF graphics library for DOS source code is
provided under the terms of GPLv2 (or later).
See lopif/copying.txt.

## Installation


### Linux / BSD

To build the SDL2 version, run "make" from the "sdl2" directory.

To build the SVGALIB version, run "make" from the "svgalib" directory.

I have not created a package for the support files (fonts,
icons, user interface, help and configuration files) yet,
so you need to install them manually. Start by downloading
the [Arachne GPL v1.95;GPL](https://www.glennmcc.org/aralinux/arachne-svgalib-1.95.tgz)
Linux package.

**Do not run the install script from the archive.**

**Do not run the arachne-install script, either.**

Extract the following files from the package:

```
   man/man1/arachne.1                  -> /usr/share/man/man1/
   doc/arachne/html/*                  -> /usr/share/doc/arachne/html/
   share/arachne/gui/*                 -> /usr/share/arachne/gui/
   share/arachne/ikons/*               -> /usr/share/arachne/ikons/
   share/arachne/iso-8859-1/*          -> /usr/share/arachne/iso-8859-1/
   share/arachne/iso-8859-2/*          -> /usr/share/arachne/iso-8859-2/
   share/arachne/mime.conf             -> /usr/share/arachne/mime.cfg
   share/arachne/templates/toolbar.cfg -> /usr/share/arachne/toolbar.cfg
   share/arachne/templates/entity.cfg  -> /usr/share/arachne/entity.cfg
```

Edit your new /usr/share/arachne/mime.cfg (**note the new file name**):

* in [MIME], replace the image/jpeg, image/png and image/x-png entries:

```
image/jpeg               JPG>BMP|convert $1 bmp3:$2
image/png                PNG>BMP|convert $1 bmp3:$2
image/x-png              PNG>BMP|convert $1 bmp3:$2
```

* in [ARACHNE], replace the .jpg, .jpe and .png entries:

```
file/.jpg            >BMP|convert $1 bmp3:$2
file/.jpe            >BMP|convert $1 bmp3:$2
file/.png            >BMP|convert $1 bmp3:$2
```

Create an initial configuration file in $HOME/.arachne/arachne.cfg:

```
# Arachne configuration
HomePage http://www.frogfind.com
Multitasking No
HTTPKeepAlive No
```

## Acknowledgements

* Michael Polák, for creating Arachne in the first place.
* Glenn McCorkle, for maintaining Arachne for the last 20-odd years.
* All other contributors over the years.
