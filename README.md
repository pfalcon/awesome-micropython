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
* [Education and courses](#education-and-courses)


Forks and Variants
==================

Notable Forks
-------------

There are more than 2000 forks of MicroPython on Github, and here are
a few notable ones:

* [Advanced MicroPython (codename "Pycopy")](https://github.com/pfalcon/micropython) -
by [@pfalcon](https://github.com/pfalcon/), 2nd largest (~35%) contributor
to MicroPython. Dedicated to further developing all the great features which
were initially contributed to the mainline - stream I/O interface, async
support, memory-saving APIs, etc. Also to optimizations, bugfixes and improved
documentation. Synced with the mainline, improvements contributed back.
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

Hardware-specific Forks
-----------------------

* [Raspberry Pi A/B/Zero bare-metal](https://github.com/boochow/micropython-raspberrypi)
  * Based on [@naums's fork](https://github.com/naums/micropython/commits/master)
* [RISC-V LoFive](https://github.com/mmicko/micropython)
* [MediaTek MT6260](https://github.com/xobs/micropython/)
* [Infeneon XMC](https://github.com/micropython/micropython-infineon)
* many more to come

Documentation
=============

* [README](https://github.com/micropython/micropython/blob/master/README.md) -
  Never to miss the project README, it's an entry to the MicroPython universe.
* [Project to complete the docs](http://pycopy.readthedocs.io/) -
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
* [upysh](https://pypi.org/project/micropython-upysh/) - very minimal file
  shell using Python syntax, suitable for devices even with little memory.
  [Part](https://github.com/pfalcon/micropython-lib/tree/master/upysh)
  of micropython-lib.
* [upy-shell](https://github.com/dhylands/upy-shell) - simple command line
  based shell.

On host:
* [rshell](https://github.com/dhylands/rshell) - remote shell for MicroPython.
* [mpfshell](https://github.com/wendlers/mpfshell) - simple shell based file
  explorer for Micropython based devices.
* [ampy](https://github.com/adafruit/ampy) - utility to interact with a
  MicroPython board over a serial connection.

IDEs
----

* [Thonny](https://thonny.org/) has [MicroPython suport](https://bitbucket.org/plas/thonny/wiki/MicroPython)
* [PyCharm/IntelliJ IDEA](https://plugins.jetbrains.com/plugin/9777-micropython)
  has [MicroPython support](https://blog.jetbrains.com/pycharm/2018/01/micropython-plugin-for-pycharm/)
* many more

Libraries
=========

Standard Libraries
------------------

* [micropython-lib](https://github.com/pfalcon/micropython-lib) - dozens
  of modules ported from CPython, dozens developed specifically for
  MicroPython.

Asynchronous Scheduling and I/O
-------------------------------

* [uasyncio](https://pypi.org/project/micropython-uasyncio/) (micro-asyncio) -
  MicroPython’s asynchronous scheduling library, roughly modeled after
  CPython’s asyncio. [Part](https://github.com/pfalcon/micropython-lib/tree/master/uasyncio)
  of micropython-lib.

Graphics
--------

* [framebuf](http://docs.micropython.org/en/latest/library/framebuf.html) -
  builtin module for simple device-independent graphics.

Graphical User Interfaces (GUI)
-------------------------------

* [micropython-nano-gui](https://github.com/peterhinch/micropython-nano-gui) -
  lightweight MicroPython GUI library for display drivers based on `framebuf` class

Text User Interfaces (TUI)
--------------------------

* [picotui](https://github.com/pfalcon/picotui) - Lightweight TUI widget
  toolkit with minimal dependencies. Works both in MicroPython and CPython.

Databases
---------

* [btree](https://pycopy.readthedocs.io/en/latest/library/btree.html) -
  builtin module, simple "NoSQL" database with dictionary-like interface,
  based on well-known BerkeleyDB 1.xx library. Available in both bare-metal
  and OS ports.
* [sqlite3](https://pypi.org/project/micropython-sqlite3/) -
  CPython's sqlite3 module ported to MicroPythin (for Unix port).
  [Part](https://github.com/pfalcon/micropython-lib/tree/master/sqlite3)

Protocols
---------

* HTTP
  * [urequests](https://pypi.org/project/micropython-urequests/) (micro-requests) -
    implements a subset of API of well-known "requests" module.
    [Part](https://github.com/pfalcon/micropython-lib/tree/master/urequests) of
    micropython-lib.

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
* [jni](https://github.com/pfalcon/micropython/blob/pfalcon/ports/unix/modjni.c) -
  Module for JavaVM integration (using JNI).
* [micropython-ffigen](https://github.com/pfalcon/micropython-ffigen) -
  Automatically generate bindings for `ffi`/`uctypes` modules from C header
  files.
* [micropython-wrap](https://github.com/stinos/micropython-wrap) -
  C++ wrapper to interface C++ code with MicroPython easily.

Textual Data Processing
-----------------------

* Regular expressions
  * [ure](https://pycopy.readthedocs.io/en/latest/library/ure.html) (micro-re) -
    builtin module which implements subset of regular expression syntax.
  * [re-pcre](https://pypi.org/project/micropython-re-pcre/) -
    more complete regular expression implementation, based on PCRE library,
    largely compatible with full CPython re syntax.
* Templating
  * [utemplate](https://github.com/pfalcon/utemplate) - Micro template engine
    with low memory usage, based on generators.

Education and courses
=====================

* University of California, Berkeley. [EE 49: Electronics for IoT](https://people.eecs.berkeley.edu/~boser/courses/49/index.html).
