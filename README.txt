Quick Start:

1. Make the environment for building Siod (with Docker)
    1.1 Download docker image with the command "docker pull deriito/siod-v3.6-buildenv:0.1"
    1.2 Use the image to start a docker container

2. Download this source code
    sh-5.1# > cd
    sh-5.1# > git clone git@github.com:deriito/siod-v3.6.git

3. Building & Installing
    sh-5.1# > cd siod
    sh-5.1# > make linux
    sh-5.1# > make install

4. Run Siod in command line
    sh-5.1# > siod
    sh-5.1# > (print "Hello World!")

=======================================================================================================
Update History:

* Edited on 2022.08.10:
The implement of "assert-dead(p)" in the thesis called "GC assertions[1]" has been implemented
in the brach "main" of this project. You can use it to assert the object which should be "dead"
in your source code. For more information, please see the original thesis.

[1] Aftandilian, Edward E., and Samuel Z. Guyer.
    "GC assertions: Using the garbage collector to check heap properties."
    Proceedings of the 30th ACM SIGPLAN Conference on Programming Language Design and Implementation.
    2009.

* Edited on 2022.07.25:
This is the lastest version 3.6 of Siod, downloaded from http://people.delphiforums.com/gjc//siod.html

=======================================================================================================
Original "README.txt" is as following:

=======================================================================================================

This is version 3.4 of Siod, Scheme In One Defun.

It is a small implementation of the Scheme programming language
with some database, unix programming and cgi scripting extensions.
The runtime footprint of the basic system is fairly small, with
the libsiod shared library linking to about 70kbytes of code on a
VAX using the standard DEC compilers for VMS. Results on other processor
architectures should scale accordingly.

George Carrette, June 16, 1996. gjc@world.std.com

The standard distribution contains unix manual pages in source
and text (txt) formats. A number of command files are provided that
invoke the interpreter to perform useful and/or exemplary tasks.
Support files and extensions 

Building: 

  unix .... the makefile has different targets for common
            operating system variants, and has been tested on all systems
            included in file.
   vms .... descrip.mms or makefile.com. The linker-options files
            provided are for VAX architecture implementations.
 win32 .... i.e. Windows 95 and Windows NT. use make.bat
            This makes a dll that can be used from any application,
            and a main console-mode program, siod.exe
 mac   .... The THINK C siod project must include siod.c,slib.c,slib.c,
            sliba.c, siodm.c, ANSI. The compilation option require 
            prototypes is recommended. Hasn't been tested with release 3.2
 amiga .... probably still works with minor source modifications.

References: comp.compilers, sunsite siod.lsm

Documentation:

siod.html is a sectionalized/cross-linked document in hyper text markup
language covering language built-in procedures, extensions, and
how to write extensions and use the shared library libsiod
from other C programs. But refer to the manual pages for
command line flags and parameters.

Updates:

The most recent version can usually be obtained from
the location http://people.delphi.com/gjc/siod.html or
ftp://ftp.std.com/pub/gjc/siod.tgz

----------------------------------------------------------------------

Entry in the free database catalog from idiom.berkeley.ca.us

David Muir Sharnoff <free-databases@idiom.berkeley.ca.us>

name:		SIOD (Scheme In One Defun/Day)
version:	3.4
interface from: C, C++, Scheme, WEB CGI.
interface to:	Oracle, RDB, flat ascii, flat binary. Sybase. MSQL.
access methods: flat files contain symbolic expression such as hash tables.
multiuser:	yes with commercial DB, no with flat files.
transactions:	yes with commercial DB, no with flat files.
distributed:	yes with commercial DB, no with flat files.
query language: SQL, any SCHEME program.
limits:		None.
robustness:	?
description:	This is a scheme interpreter with built-in procedures using
		the Oracle Call Interface (OCI) and RDB SQL Services.
		You can use it merely as a flexible database loader/unloader
		with fast binary flat-file data save/restore. Or you can
		use it to apply the classic Symbolic Manipulation or
		Artificial Intelligence techniques on your data sets.
		The main-program can be oriented towards batch, character-cell
		terminal, or Window/GUI. Sybase via ct library.
                The system also provides a general purpose unix scripting 
                language environment.
references:	Structure and Interpretation of Computer Programs MIT Press.
announcements:	comp.lang.scheme, comp.databases.rdb, comp.databases.oracle
bugs:		Contact the author.
requires:	C compiler, your favorite commercial DB. Posix regular
                expression library.    
ports:		VMS, WINDOWS NT, UNIX, OS/2, MACINTOSH. LINUX. OSF/1. SGI.
                WINDOWS 95. SOLARIS.
author:		George Carrette <gjc@world.std.com>
how to get:	http://people.delphi.com/gjc/siod.html has instructions.
                Also ftp://ftp.std.com/pub/gjc.
updated:	1997/04/03
