# Crypto Ancienne: TLS for the Internet of Old Things
## This repository is a fork of [Crypto Ancienne](https://github.com/classilla/cryanc).
Copyright (C) 2020-3 Cameron Kaiser and Contributors. All rights reserved.

## Difference

Since Crypto Ancienne cannot run natively under classic Mac OS I always wanted to run it on a raspberry pi to be used as the proxy within Classilla. 

## Changes

- Added the file micro_inetd.c
- Removed alias for socklen_t in micro_inetd.c

## Prerequisites

- Raspberry Pi: I ran this on the first model with only 128mb of ram so any should do.
- Classilla 9.3.4b: You can download it [here](https://sourceforge.net/projects/classilla/files/9.3.4b/).

## Instructions

1. `git clone https://github.com/harryfornasier/cryanc-raspberry-pi.git`
2. `cd cryanc-raspberry-pi`
3. `gcc -O3 -o carl carl.c`
5. `cc -DPROMISCUOUS -O3 -o micro_inetd_any micro_inetd.c`
6. `./micro_inetd_any 8765 ./carl -p`

Crypto Ancienne should be running now for you to use as a proxy in Clasilla. Follow the [Configuring and Using Classilla](https://www.floodgap.com/software/classilla/carl.html) guide to set it up.

## Licenses and copyrights

Crypto Ancienne is released under the BSD license.

Copyright (C) 2020-3 Cameron Kaiser and Contributors. All rights reserved.

Based on TLSe. Copyright (C) 2016-2023 Eduard Suica. All rights reserved.

Based on Adam Langley's implementation of Curve25519. Copyright (C) 2008 Google, Inc. All rights reserved.

Based on OpenBSD's `arc4random` (allegedly). Copyright (C) 1996 David Mazieres. All rights reserved.

Based on `libtomcrypt` by Tom St Denis and contributors. Unlicense.

Based on public domain works by D. J. Bernstein.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
