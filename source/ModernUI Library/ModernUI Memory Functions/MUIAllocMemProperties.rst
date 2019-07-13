.. _MUIAllocMemProperties:

========================
MUIAllocMemProperties 
========================

MUIAllocMemProperties, hWin::ref:`MUIWND<MUIWND>`, cbWndExtraOffset::ref:`MUIPROPERTIES<MUIPROPERTIES>`, SizeToAllocate::ref:`MUIVALUE<MUIVALUE>`

Allocates memory for the internal or external properties storage - typically during `WM_CREATE <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-create>`_ event and this memory is freed by a call to the :ref:`MUIFreeMemProperties<MUIFreeMemProperties>` function during `WM_DESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-destroy>`_ or `WM_NCDESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-ncdestroy>`_ event.

**Parameters**

* [in] **hWin** - handle to the ModernUI control
* [in] **cbWndExtraOffset** - offset in the `WNDCLASS.cbWndExtra  <https://docs.microsoft.com/en-us/windows/win32/api/winuser/ns-winuser-tagwndclassa>`_ memory location. For ease of use, the following constants can be used: ``MUI_INTERNAL_PROPERTIES`` or ``MUI_EXTERNAL_PROPERTIES``
* [in] **SizeToAllocate** - size of memory block

**Return**

Returns ``TRUE`` if successful or ``FALSE`` otherwise

**Example**

::

   ; MyControl.inc:

   ; external properties for user of control
   ; defined in public user MyControl.inc file
   @MyControlTextColor EQU 0
   @MyControlBackColor EQU 4
   @MyControlSpecial   EQU 8
   
::

   ; MyControl.asm:

   ; external properties storage for control
   ; defined inside developer MyControl.asm source file
   MUI_MYCONTROL  STRUCT
     dwTextColor  DD ?
     dwBackColor  DD ?
     bSpecial     DD ?
   MUI_MYCONTROL  ENDS
   
   ; internal properties storage for control
   ; defined inside developer MyControl.asm source file
   _MUI_MYCONTROL STRUCT
     dwEnabled    DD ?
     dwMouseOver  DD ?
   _MUI_MYCONTROL ENDS
   
   ; Define internal properties
   ; for developer use in the MyControl.asm source file
   @MyControlEnabled   EQU 0
   @MyControlMouseOver EQU 4

::

   ; MyControl.asm:
   
   .ELSEIF eax == WM_CREATE
      ; Alloc internal and external property storage for MyControl
      Invoke MUIAllocMemProperties, MUI_INTERNAL_PROPERTIES, SIZEOF _MUI_MYCONTROL
      Invoke MUIAllocMemProperties, MUI_EXTERNAL_PROPERTIES, SIZEOF MUI_MYCONTROL
      mov eax, TRUE
      ret


**See Also**

:ref:`MUIFreeMemProperties<MUIFreeMemProperties>`, :ref:`MUIAllocStructureMemory<MUIAllocStructureMemory>`, `WM_CREATE <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-create>`_, `WM_DESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-destroy>`_, `WM_NCDESTROY <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-ncdestroy>`_, `WNDCLASS  <https://docs.microsoft.com/en-us/windows/win32/api/winuser/ns-winuser-tagwndclassa>`_

