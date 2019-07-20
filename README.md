Awesome MicroPython
===================

<p align="center">
  <img src="https://raw.githubusercontent.com/micropython/micropython/master/logo/micropythonpowered-art.png" alt="MicroPython Powered"/>
</p>

[MicroPython](https://micropython.org) came known as a "Python for
microcontrollers". It's far more than that.

MicroPython is a full-stack language, which, unlike many other languages,
is concerned not only with scaling up, but also with scaling down. This
means it can run on your laptop, desktop, on a supercomputer (sure, why
not), but also inside your Internet router, fridge, clock, smartwatch,
temperature sensor, microcontroller development board, inside your new
game or productivity app, and in gazillion of other applications and
devices. Familiar, easy to use, expressive language everywhere, with
the ability to optimize your software based on the hardware needs.

Summing this all up with the (unoffical) motto: **MicroPython runs everywhere!**

MicroPython is created and maintained by Damien George,
[@dpgeorge](https://github.com/dpgeorge/).

This list is not directly affiliated with, or endorsed by, the "official"
MicroPython and/or forks owned by other parties. Opinions here are solely
those of the list author and agreeing contributors. The list is intended
to capture breadth and pluralism of the MicroPython community, but may
be subjective nonetheless.

This list is compiled and maintained by Paul Sokolovsky, [@pfalcon](https://github.com/pfalcon/).
This list is licensed under [Creative Commons Attribution-ShareAlike 4.0 
International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/):
you are free to share and reuse contents of this list, as long as you
give credit to the original author and allow other people to share/reuse
it under the same terms.

* [Forks and Variants](#forks-and-variants)
* [Documentation](#documentation)
* [Tools](#tools)
* [Libraries](#libraries)
* [Learning MicroPython](#learning-micropython)


Forks and Variants
==================

Notable Forks
-------------

There are more than 2000 forks of MicroPython on Github, and here are
a few notable ones:

* [Pycopy](https://github.com/pfalcon/pycopy) -
by [@pfalcon](https://github.com/pfalcon/), 2nd largest (~35%) contributor
to MicroPython. Dedicated to further developing all the great features which
were initially contributed to the mainline - stream I/O interface, async
support, memory-saving APIs, etc. Also to optimizations, bugfixes and improved
documentation. Synced with the mainline.
* [Pycom MicroPython](https://github.com/pycom/pycom-micropython-sigfox) -
by [@pycom](https://github.com/pycom/). Support for modern communication
standards like LoRa, Sigfox, etc.
* [CircuitPython](https://github.com/adafruit/circuitpython) -
by [@adafruit](https://github.com/adafruit/). Education friendly MicroPython
fork, concentrating on microcontroller boards of a particular vendor.
Wealth of online tutorials and educational resources.
* [OpenMV](https://github.com/openmv/openmv) - by [@openmv](https://github.com/openmv).
MicroPython fork for machine vision boards.
* [Loboris ESP32 fork](https://github.com/loboris/MicroPython_ESP32_psRAM_LoBo) -
by [@loboris](https://github.com/loboris). Concentrates on ESP32. A number
of C libraries are wrapped.

OS/RTOS Ports/Forks
-------------------

* POSIX/Unix - part of the mainline. The POSIX port is the biggest and most
important MicroPython target, alone supporting thousands of diverse computer
and device types, ranging from supercomputers to a few-dollar appliances.
* Windows - part of the mainline. Runs on different Windows variants, from
Server down to Windows IoT.
* DOS/DJGPP - part of the mainline. Runs on DOS versions with support of x86
extended mode.
* [Zephyr port](https://github.com/pfalcon/micropython) - Modern advanced RTOS,
more than 100 boards supported.
* FreeRTOS port - part of the mainline (as CC3200 port).
* [mbedOS port](https://os.mbed.com/users/infinnovation/code/micropython/) -
RTOS for ARM microcontrollers, dozens of boards supported.
* [FrostedOS port](https://github.com/insane-adding-machines/micropython) -
POSIX-compatible RTOS.
* [UEFI port](https://github.com/tianocore/tianocore.github.io/wiki/MicroPython) -
port to UEFI (BIOS replacement framework) by Intel
([ANN](https://software.intel.com/en-us/blogs/2018/03/08/implementing-micropython-as-a-uefi-test-framework)).

Hardware-specific Forks
-----------------------

* [Raspberry Pi A/B/Zero bare-metal](https://github.com/boochow/micropython-raspberrypi)
  * Based on [@naums's fork](https://github.com/naums/micropython/commits/master)
* [RISC-V LoFive](https://github.com/mmicko/micropython)
* [MediaTek MT6260](https://github.com/xobs/micropython/)
* [Infeneon XMC](https://github.com/micropython/micropython-infineon)
* [NXP i.MX RT/LPC546](https://github.com/RockySong/micropython-rocky)
* many more to be listed

Documentation
=============

* [README](https://github.com/micropython/micropython/blob/master/README.md) -
  Never to miss the project README, it's an entry to the MicroPython universe.
* [Pycopy docs](http://pycopy.readthedocs.io/) are more complete -
  Online searchable documentation for language aspects and builtin modules.
* [Mainline docs](http://docs.micropython.org/) lag in updates.
* [CPython 3.5 docs](https://docs.python.org/3.5/) - MicroPython is an
  implementation of the Python language, so main Python docs provide
  the relevant background information (MicroPython's own docs concentrate
  on differences with CPython and new features added.)

Tools
=====

Accessing MicroPython Prompt (REPL)
-----------------------------------

* Local access: MicroPython comes with REPL (read-evaluate print loop,
interactive prompt), which you can access right in your terminal, or by
connecting over UART (serial) or USB to another device.
* Remote access:
  * Telnet - available for some ports (e.g. CC3200), 3rd-party libraries
    for other ports.
  * WebREPL - REPL in your browser using Websockets! Official client:
    http://micropython.org/webrepl/ . Can be
    [deployed locally](https://github.com/micropython/webrepl/).

Shells
------

There're shells which run directly on a MicroPython device (or in a MicroPython
process), and ones whict run on a host and connect to a device:

On device:
* [upysh](https://pypi.org/project/pycopy-upysh/) - very minimal file
  shell using Python syntax, suitable for devices even with little memory.
  [Part](https://github.com/pfalcon/pycopy-lib/tree/master/upysh)
  of pycopy-lib.
* [upy-shell](https://github.com/dhylands/upy-shell) - simple command line
  based shell.

On host:
* [rshell](https://github.com/dhylands/rshell) - remote shell for MicroPython.
* [mpfshell](https://github.com/wendlers/mpfshell) - simple shell based file
  explorer for Micropython based devices.
* [ampy](https://github.com/adafruit/ampy) - utility to interact with a
  MicroPython board over a serial connection.

Package Management
------------------

* Packages are distributed via [Python Package Index (PyPI)](https://pypi.org/search/?q=micropython),
  like packages for any other Python implementation.
* Installable using [upip](https://github.com/pfalcon/pycopy-lib#usage)
  package manager (built into Unix port and some other ports with
  networking capabilities, part of pycopy-lib otherwise).
* Documentation of [MicroPython package usage](https://pycopy.readthedocs.io/en/latest/reference/packages.html)
  * For non-networked ports, packages can be "cross-installed" on a host,
    and copied to device (manually or using host-side shells above).
  * For ultimate RAM efficiency, packages can be "frozen" into MicroPython
    binary.

IDEs
----

* [Thonny](https://thonny.org/) has [MicroPython suport](https://bitbucket.org/plas/thonny/wiki/MicroPython)
* [PyCharm/IntelliJ IDEA](https://plugins.jetbrains.com/plugin/9777-micropython)
  has [MicroPython support](https://blog.jetbrains.com/pycharm/2018/01/micropython-plugin-for-pycharm/)
* [Mu Editor](https://github.com/mu-editor/mu)
* many more

Libraries
=========

Standard Libraries
------------------

* [pycopy-lib](https://github.com/pfalcon/pycopy-lib) - Standard library
  of the Pycopy project. Dozens of modules ported from CPython, dozens
  developed specifically for Pycopy.
* [Backports of Pycopy API modules to CPython](https://github.com/pfalcon/pycopy-lib#cpython-backports) -
  Allows to run software written for MicroPython using CPython (WIP). Part
  of pycopy-lib.

Asynchronous Scheduling and I/O
-------------------------------

* [uasyncio](https://pypi.org/project/pycopy-uasyncio/) (micro-asyncio) -
  Pycopy’s asynchronous scheduling library, roughly modeled after
  CPython’s asyncio. [Part](https://github.com/pfalcon/pycopy-lib/tree/master/uasyncio)
  of pycopy-lib.

Graphics
--------

* [framebuf](http://docs.micropython.org/en/latest/library/framebuf.html) -
  builtin module for simple device-independent graphics.

Graphical User Interfaces (GUI)
-------------------------------

* [micropython-nano-gui](https://github.com/peterhinch/micropython-nano-gui) -
  lightweight MicroPython GUI library for display drivers based on `framebuf` class
* [LittlevGL bindings](https://github.com/littlevgl/lv_binding_micropython) -
  Bindings for [LittlevGL](https://littlevgl.com/) GUI library (C).

Text User Interfaces (TUI)
--------------------------

* [picotui](https://github.com/pfalcon/picotui) - Lightweight TUI widget
  toolkit with minimal dependencies. Works both in MicroPython and CPython.
* [FBConsole](https://github.com/boochow/FBConsole) - MicroPython terminal
  (dupterm) over framebuffer.

Databases
---------

* [btree](https://pycopy.readthedocs.io/en/latest/library/btree.html) -
  builtin module, simple "NoSQL" database with dictionary-like interface,
  based on well-known BerkeleyDB 1.xx library. Available in both bare-metal
  and OS ports.
* [sqlite3](https://pypi.org/project/pycopy-sqlite3/) -
  Reimplementation of CPython's sqlite3 module for Pycopy (Unix port).
  [Part](https://github.com/pfalcon/pycopy-lib/tree/master/sqlite3) of pycopy-lib.
* [micropython-redis](https://github.com/dwighthubbard/micropython-redis) -
  Redis client.
* [picoredis](https://github.com/SpotlightKid/picoredis) -
  Another Redis client.
* [uPyMySQL](https://github.com/dvrhax/uPyMySQL) - MySQL client.

Protocols
---------

* HTTP
  * [urequests](https://pypi.org/project/pycopy-urequests/) (micro-requests) -
    implements a subset of API of well-known "requests" module.
    [Part](https://github.com/pfalcon/pycopy-lib/tree/master/urequests) of
    pycopy-lib.

* DNS
  * [udnspkt](https://pypi.org/project/pycopy-udnspkt/) - DNS queries,
    [Sans I/O](https://sans-io.readthedocs.io/) approach.
    [Part](https://github.com/pfalcon/pycopy-lib/tree/master/udnspkt) of
    pycopy-lib.

* Websocket
  * [websocket](https://github.com/pfalcon/micropython/blob/pfalcon/extmod/modwebsocket.c) - 
  builtin provisional module (i.e. details of API is subject to change).

Web Frameworks
--------------

* [picoweb](https://github.com/pfalcon/picoweb/) - Really minimal web
  application framework based on "uasyncio" module.

Interfacing with Other Languages
--------------------------------

* [ffi](https://pycopy.readthedocs.io/en/latest/library/ffi.html) -
  Foreign Function Interface module for MicroPython. Call C, etc. functions
  from dynamic libraries or just in memory.
* [uctypes](https://pycopy.readthedocs.io/en/latest/library/uctypes.html) -
  "Foreign Data" interface for MicroPython. Access binary data structures
  with the expressiveness of C language. "ffi" and "uctypes" modules commonly
  used together.
* [jni](https://github.com/pfalcon/pycopy/blob/pfalcon/ports/unix/modjni.c) -
  Module for JavaVM integration (using JNI).
* [pycopy-ffigen](https://github.com/pfalcon/pycopy-ffigen) -
  Automatically generate bindings for `ffi`/`uctypes` modules from C header
  files.
* [micropython-wrap](https://github.com/stinos/micropython-wrap) -
  C++ wrapper to interface C++ code with MicroPython easily.
* [ullvm](https://github.com/pfalcon/ullvm) - Bindings for LLVM C API.

Textual Data Processing
-----------------------

* Regular expressions
  * [ure](https://pycopy.readthedocs.io/en/latest/library/ure.html) (micro-re) -
    builtin module which implements subset of regular expression syntax.
  * [re-pcre](https://pypi.org/project/pycopy-re-pcre/) -
    more complete regular expression implementation, based on PCRE library,
    largely compatible with full CPython re syntax.
* Templating
  * [utemplate](https://github.com/pfalcon/utemplate) - Micro template engine
    with low memory usage, based on generators.

Sciences
--------

* [uMath](https://github.com/AaronKel/uMath) - Symbolic computer algebra system
  (CAS)

Learning MicroPython
====================

Sites
-----

* [MicroPython category in Adafruit Learning System](https://learn.adafruit.com/category/micropython)

Books
-----

* [Programming with MicroPython: Embedded Programming with Microcontrollers and Python](https://books.google.com/books/about/Programming_with_MicroPython.html?id=Bic3DwAAQBAJ),
  Nicholas H. Tollervey, 2017
* [MicroPython for the Internet of Things: A Beginner’s Guide to Programming with Python on Microcontrollers](https://books.google.com/books/about/MicroPython_for_the_Internet_of_Things.html?id=70NADwAAQBAJ),
  Charles Bell, 2017

Academia
--------

* University of California, Berkeley. [EE 49: Electronics for IoT](https://people.eecs.berkeley.edu/~boser/courses/49/index.html).

