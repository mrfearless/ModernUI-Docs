.. _MUIFreeMemProperties:

========================
MUIFreeMemProperties 
========================

**MUIFreeMemProperties, hControl:HWND, cbWndExtraOffset:SIZE_T**

Frees memory allocated via the :ref:`MUIAllocMemProperties<MUIAllocMemProperties>` function. Used at the `WM_DESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-destroy>`_ or `WM_NCDESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-ncdestroy>`_ event. Make sure any cleanup routines are called before freeing any memory.

**Parameters**

* [in] **hControl** - handle to the ModernUI control
* [in] **cbWndExtraOffset** - offset in the `WNDCLASS.cbWndExtra  <https://docs.microsoft.com/en-us/windows/win32/api/winuser/ns-winuser-tagwndclassa>`_ memory location. For ease of use, the following constants can be used: ``MUI_INTERNAL_PROPERTIES`` or ``MUI_EXTERNAL_PROPERTIES``

**Return**

Returns ``TRUE`` if successful or ``FALSE`` otherwise

**Example**

::

   ; MyControl.asm:
   
   .ELSEIF eax == WM_DESTROY
      ; Cleanup before freeing memory
      Invoke MyControlCleanup, hWin
      ; Free internal and external property storage memory for MyControl
      Invoke MUIFreeMemProperties, MUI_INTERNAL_PROPERTIES
      Invoke MUIFreeMemProperties, MUI_EXTERNAL_PROPERTIES
      mov eax, 0
      ret


**See Also**

:ref:`MUIAllocMemProperties<MUIAllocMemProperties>`, :ref:`MUIAllocStructureMemory<MUIAllocStructureMemory>`, `WM_DESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-destroy>`_, `WM_NCDESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-ncdestroy>`_, `WNDCLASS  <https://docs.microsoft.com/en-us/windows/win32/api/winuser/ns-winuser-tagwndclassa>`_

