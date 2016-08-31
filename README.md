# OpenVG
These are the official Khronos Group OpenVG headers for OpenVG 1.1.

The goal of this repository is not to contain code files, but only header files of the latest
OpenVG specification from the registry.

Additional modifications are to be provided in the `<VG/vgext.h>` file to support 3rd party extensions as well as
platform support in `<VG/vgplatform.h>`. These mods might not be official, but updates that will help people supporting
OpenVG with their renderer implementation.

Note: As maintainer for this github repo, I do not claim ownership of these headers. I'm not in the Khronos Group,
nor claim to be well versed in the arcane OpenVG arts. I just need this in GitHub, and thought it might be useful to others.
For the original, more information and the reference implementation, please look here: https://www.khronos.org/registry/vg/

## Building goal

Many platforms don't support OpenVG by default. The headers `<VG/*>` aren't available on the system. But then, multiple 3rd party
services offer support through their own implementation of the OpenVG system.

This repository contains these headers, alongside extensions required to run these 3rd party (and often open-source) implementation.

If you wish to create a makefile for your plaform, make sure it installs the .h files in the project's system-level headers, as included through the <> brackets. You should be able to do `#include <VG/openvg.h>`

If your plaform requires supplemental includes, please add them to `<VG/vgplatform.h>`

If you wish to add OpenVG extensions for your implementations, please add them to `<VG/vgext.h>`.

## My commitment

**Remember I am not the official maintainer for Khronos OpenVG! If you want to really officialize things, please take your extensions to the Khronos Groups! I just wish to help!**

If the Khronos group sends updates to their headers, I will merge it to this repo. These updates have precedence over everything else, including backward compatibility. They are the Gods for this project!

At the same time, if any OpenVG user wishes to push their extension to their working system, I will gladly add them as soon as I have some time.
