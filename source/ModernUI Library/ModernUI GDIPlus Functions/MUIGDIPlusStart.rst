.. _MUIGDIPlusStart:

========================
MUIGDIPlusStart 
========================

**MUIGDIPlusStart**

Start of ModernUI **GDI+** framework (wrapper for `GdiplusStartup <https://docs.microsoft.com/en-us/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup>`_). Placed at start of program before WinMain call or during creation of a ModernUI control during a `WM_CREATE <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-create>`_ event.

**Parameters**

None


**Return**

None

**Example**

::

   Invoke MUIGDIPlusStart


::

   Invoke MUIGDIPlusStart ; Start GDI+ before program starts
   Invoke WinMain, hInstance, NULL, CommandLine, SW_SHOWDEFAULT
   Invoke MUIGDIPlusFinish ; Finish GDI+ as program exits
   Invoke ExitProcess, eax


::

   .ELSEIF eax == WM_CREATE
      Invoke MUIAllocMemProperties, hWin, MUI_INTERNAL_PROPERTIES, SIZEOF _MUI_MYCONTROL_PROPERTIES
      Invoke MUIAllocMemProperties, hWin, MUI_EXTERNAL_PROPERTIES, SIZEOF MUI_MYCONTROL_PROPERTIES 
      Invoke MUIGDIPlusStart ; Start GDI+
      Invoke _MUI_MyControlInit, hWin
      mov eax, 0
      ret    
   
   .ELSEIF eax == WM_NCDESTROY
      Invoke _MUI_MyControlCleanup, hWin
      Invoke MUIFreeMemProperties, hWin, MUI_INTERNAL_PROPERTIES
      Invoke MUIFreeMemProperties, hWin, MUI_EXTERNAL_PROPERTIES
      Invoke MUIGDIPlusFinish ; Finish GDI+
      mov eax, 0
      ret


**See Also**

:ref:`MUIGDIPlusFinish<MUIGDIPlusFinish>`, `WM_CREATE <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-create>`_, `GdiplusStartup <https://docs.microsoft.com/en-us/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup>`_

