.. _MUIGDIPlusFinish:

========================
MUIGDIPlusFinish 
========================

MUIGDIPlusFinish

Finish ModernUI **GDI+** framework (wrapper for `GdiplusShutdown <https://docs.microsoft.com/en-us/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusshutdown>`_). Placed after WinMain call before ExitProcess or during exit of a ModernUI control during a `WM_DESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-destroy>`_ or a `WM_NCDESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-ncdestroy>`_ event


**Parameters**

None

**Return**

None

**Example**

::

   Invoke MUIGDIPlusFinish


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

:ref:`MUIGDIPlusStart<MUIGDIPlusStart>`, `WM_DESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-destroy>`_, `WM_NCDESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-ncdestroy>`_, `GdiplusShutdown <https://docs.microsoft.com/en-us/windows/win32/api/gdiplusinit/nf-gdiplusinit-gdiplusshutdown>`_

