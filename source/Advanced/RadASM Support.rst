==============
RadASM Support
==============

RadASM auto-complete / intellisense api files and some design time ModernUI UI controls for RadASM are available to help with using the various ModernUI functions and controls.

-----------------------------------
RadASM auto-complete / intellisense
-----------------------------------

RadASM can support multiple languages. For developing for x86 it is recommended to use the `MASM32 assembler <http://www.masm32.com/download.htm>`_. For x64 development it is recommended to use the `UASM assembler <http://www.terraspace.co.uk/uasm.html>`_.

MASM32 x86 assembler auto-complete / intellisense files:

* masmApiCall.api.txt
* masmApiConst.api.txt
* masmApiStruct.api.txt
* masmMessage.api.txt

UASM x64 assembler auto-complete / intellisense files:

* Uasm64ApiCall.api.txt
* Uasm64ApiConst.api.txt
* Uasm64ApiStruct.api.txt
* Uasm64Message.api.txt

Each ``.api.txt`` file can be opened and the contents copied and pasted into a corresponding ``.api`` file found under the RadASM folder for the particular assembler. Once RadASM is restarted it will read these files and provide the auto-complete / intellisense for ModernUI functions.


------------------------------------
RadASM Design Time ModernUI Controls
------------------------------------

A RAMUIControls.zip file is provided in the ModernUI repository in the release section that contains a collection of the design time ModernUI controls for RadASM. Each control is provided for in a separate dll file.

The current ModernUI controls that have a RadASM IDE control are:

* ModernUI_Button (RAMUIButton.dll)
* ModernUI_CaptionBar (RAMUICaptionBar.dll)
* ModernUI_Checkbox (RAMUICheckbox.dll)
* ModernUI_ProgressBar (RAMUIProgressBar.dll)
* ModernUI_ProgressDots (RAMUIProgressDots.dll)
* ModernUI_SmartPanel (RAMUISmartPanel.dll)
* ModernUI_Spinner (RAMUISpinner.dll)
* ModernUI_Text (RAMUIText.dll)

**Installation**

* Ensure RadASM is closed before installing the design time ModernUI controls.
* Copy the RAMUIxxxxxxxxx.dll files to your RadASM folder
* Edit **RadASM.ini** and add the controls to the section entitled ``[CustCtrl]``. Each entry should be a unique number in sequential order.

Once completed it should look something like this:

::

   [CustCtrl]
   1=RAMUIButton.dll
   2=RAMUICaptionBar.dll
   3=RAMUICheckbox.dll
   4=RAMUIProgressBar.dll
   5=RAMUIProgressDots.dll
   6=RAMUISmartPanel.dll
   7=RAMUIText.dll
   8=RAMUISpinner.dll


**Usage**

Once the design time ModernUI controls are installed (and RadASM is restarted) they will show up as icons in the dialog tools/toolbox toolbar.
These provide a visual way of adding the ModernUI controls to your project and setting a few properties 

It is important to note that the dll files that contain each ModernUI control is not a full version of the tool, merely enough to provide a visual representation of the tool when added to a dialog. You still have to include the appropriate library and include files AND call to register the ModernUI control before the dialog is created. Typically this registration should be done at the start of your program

For example if you wish to use the ModernUI_CaptionBar control and add it to a dialog, you should also place a call to register this control at start, something like:

::

   start:
   
      Invoke GetModuleHandle,NULL
      mov hInstance, eax
      Invoke GetCommandLine
      mov CommandLine, eax
      Invoke InitCommonControls
      mov icc.dwSize, sizeof INITCOMMONCONTROLSEX
      mov icc.dwICC, ICC_COOL_CLASSES or ICC_STANDARD_CLASSES or ICC_WIN95_CLASSES
      Invoke InitCommonControlsEx, offset icc
      
      ; Register the control so that when the dialog that contains it is created
      ; it knows where to find the CaptionBar control.
      Invoke MUICaptionBarRegister
      
      Invoke WinMain, hInstance, NULL, CommandLine, SW_SHOWDEFAULT
      Invoke ExitProcess, eax



----------------
RadASM with UASM
----------------

The ModernUI x64 Library and ModernUI x64 Controls come with a RadASM project to help build the sources. To fully utilize this you may need to download and install:

* `UASM with RadASM <https://github.com/mrfearless/UASM-with-RadASM>`_

and either:

* `UASM-SDK <https://github.com/mrfearless/UASM-SDK>`_

or

* `UASM <http://www.terraspace.co.uk/uasm.html>`_
* `WinInc <http://www.terraspace.co.uk/WinInc209.zip>`_
* 64bit libraries - Can be obtained via: (assuming default installed locations)

  * Installed Windows SDK: ``\Program Files (x86)\Microsoft SDKs\Windows\v7.1A\Lib\x64``
  * Installed Windows Kit: ``\Program Files (x86)\Windows Kits\8.1\Lib\winv6.3\um\x64``
  * PellesC - ``\PellesC\Lib\Win64``
  
* Other Binaries: 

  * Resource Compiler: ``rc.exe``, ``rcdll.dll``
  * Resource Converter: ``cvtres.exe``, ``cvtres.exe.config``
  * Linker & Lib Manager: ``lib.exe``, ``link.exe``, ``link.exe.config``, ``msobj120.dll``, ``mspdb120.dll``, ``mspdbcore.dll`` and the c runtime ``msvcr120.dll``


The UASM assembler and all related files (includes, libs, x64 libs, other binaries) should be placed in the appropriate folders so that your installation matches the following folder structure:

::

   \UASM\bin
   \UASM\include
   \UASM\lib
   \UASM\lib\x64


To add support for the UASM assembler to RadASM download and extract the `UASM with RadASM <https://github.com/mrfearless/UASM-with-RadASM>`_ package and edit the **RadASM.ini** file to add UASM32 and UASM64 to the Assembler entry under the Assembler section:

::

   [Assembler]
   Assembler=masm,UASM32,UASM64,JWasm,GoAsm,fasm,nasm,html


The RadASM projects for the ModernUI x64 Library and ModernUI x64 Controls should now assemble if all the above steps have been taken.