.. _ModernUI x86 Build:

==================
ModernUI x86 Build
==================

The ModernUI Library and ModernUI Controls come with a RadASM project to help build the sources. However if you wish to build them manually here are the command line options you should use.

-------------------------
Building ModernUI Library
-------------------------

The ModernUI Library consists of two files:

- ModernUI.inc
- ModernUI.asm

Building with Microsoft MASM (ML.EXE):

.. code-block:: text

   ML.EXE /c /coff /Cp /nologo /I"X:\MASM32\Include" ModernUI.asm


*X: is the drive letter where your MASM32 SDK includes files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*

Linking with Microsoft Library Manager (LIB.EXE):

.. code-block:: text

   LIB *.obj /out:ModernUI.lib


--------------------------
Building ModernUI Controls
--------------------------

Each ModernUI Control consists of two files:

- ModernUI_Control.inc
- ModernUI_Control.asm


Building with Microsoft MASM (ML.EXE):

.. code-block:: text

   ML.EXE /c /coff /Cp /nologo /I"X:\MASM32\Include" ModernUI_Control.asm


\*X: *is the drive letter where your MASM32 SDK includes files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*

Linking with Microsoft Library Manager (LIB.EXE):

.. code-block:: text

   LIB *.obj /out:ModernUI_Control.lib
   

----------------
Debug x86 Builds
----------------

To build the ModernUI Library and/or a ModernUI Control with debug information, supply the additional flag options /Zi /Zd on the command line for MASM (ML.EXE) like so:
.. code-block:: text

   ML.EXE /c /coff /Cp /Zi /Zd /nologo /I"X:\MASM32\Include" ModernUI.asm


.. code-block:: text

   ML.EXE /c /coff /Cp /Zi /Zd /nologo /I"X:\MASM32\Include" ModernUI_Control.asm


\*X: *is the drive letter where your MASM32 SDK includes files are located, replace with the appropriate drive letter for your installation, or modify the path for your installed location.*