==================
ModernUI x64 Build
==================

The ModernUI Library and ModernUI Controls come with a RadASM project to help build the sources. However if you wish to build them manually here are the command line options you should use.

-------------------------
Building ModernUI Library
-------------------------

The ModernUI Library consists of two files:

* ModernUI.inc
* ModernUI.asm

Building with Microsoft UASM (UASM64.EXE):
::

   UASM64.EXE /c -win64 -Zp8 /win64 /D_WIN64 /Cp /nologo /I"X:\UASM\Include" ModernUI.asm


\*X: *is the drive letter where your UASM SDK includes files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*

Linking with Microsoft Library Manager (LIB.EXE):

::

   LIB /LIBPATH:"X:\UASM\lib\x64" *.obj /out:ModernUI.lib


*X: is the drive letter where your UASM SDK 64bit library files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*

--------------------------
Building ModernUI Controls
--------------------------

Each ModernUI Control consists of two files:

* ModernUI_Control.inc
* ModernUI_Control.asm

Building with Microsoft UASM (UASM64.EXE):

::

   UASM64.EXE /c -win64 -Zp8 /win64 /D_WIN64 /Cp /nologo /I"X:\MASM32\Include" ModernUI_Control.asm


\*X: *is the drive letter where your UASM64 SDK includes files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*

Linking with Microsoft Library Manager (LIB.EXE):

::

   LIB /LIBPATH:"X:\UASM\lib\x64" *.obj /out:ModernUI_Control.lib


\*X: *is the drive letter where your UASM SDK 64bit library files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*

----------------
Debug x64 Builds
----------------

To build the ModernUI Library and/or a ModernUI Control with debug information, supply the additional flag options /Zi /Zd on the command line for UASM64 (UASM64.EXE) like so:

::

   UASM64.EXE /c -win64 -Zp8 /win64 /D_WIN64 /Cp /nologo /Zi /Zd /I"X:\UASM\Include" ModernUI.asm


::

   UASM64.EXE /c -win64 -Zp8 /win64 /D_WIN64 /Cp /nologo /Zi /Zd  /I"X:\UASM\Include" ModernUI_Control.asm


\*X: *is the drive letter where your UASM SDK includes files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*

Linking with Microsoft Library Manager (LIB.EXE):

::

   LIB /LIBPATH:"X:\UASM\lib\x64" *.obj /out:ModernUI_Control.lib


\*X: *is the drive letter where your UASM SDK 64bit library files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*
