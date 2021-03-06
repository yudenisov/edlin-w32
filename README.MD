EDLIN
=====

The edlin program is a small line editor, written for FreeDOS as a functional
clone of the old MS-DOS program edlin. It differs from MS edlin in that
first, it's free software, and second, the user interface is slightly
different in a few places. The reason for the difference is so that the user
does not have to type in control characters mandated by MS edlin's syntax.

It's added the Win32 fork of this program written on Visual Studio C 2017 and correctly work with long file names and NTFS file system in this project

INVOKING EDLIN
==============

The edlin program is invoked either by itself:

        edlin

or with a filename that's initially read in:

        edlin file
        
The Win32 fork of Edlin is named after `edlinw32.exe`

EDLIN'S INTERNAL COMMANDS
-------------------------

The edlin internal commands are described in the HTML file that comes in this
distro.

COMPILING EDLIN
===============

The edlin program has been tested with these compilers:

Microsoft Visual C++:
---------------------

To compile with MSVC++, first rename config-h.vscpp to config.h. Then, have
the symbol HAVE_CONFIG_H defined on the command line or in the project file.

Borland C++:
------------

Use the makefile Makefile.bc. The makefile should copy config-h.bc to config.h
before compiling.

The Japanese port uses Borland filenames. To compile it properly, the symbol 
SHIFT_JIS must be defined on the command line. It includes <dos.h>, <conio.h>,
and <jctype.h>.

GNU gcc under Cygwin:
---------------------

Compiling under Cygwin should be as easy as 

	  ./configure;make;make install

as edlin has been successfully autoconfiscated. ;-)

If you don't want to use the ./configure script, Eric Auer has noted that
after copying config-h.bc to config.h and renaming your favorite msgs-*.h
file to msgs.h,

        gcc -o edlin.exe -Wall *.c

should also work. I'm leaving the configure script and Makefile in there,
though, as the generated Makefile can also be used to install edlin and
create distros. ;-)

OpenWatcom:
-----------

To compile under OpenWatcom, just use the edlin.wpj file. It is currently set
up for 16-bit FreeDOS, but can easily be changed.

Gregory Pietsch, 2003-06-09  
Yuri Denisov, 2018-07-14

