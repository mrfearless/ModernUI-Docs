.. _MUISPM_REGISTERPANEL:

===================================
MUISPM_REGISTERPANEL 
===================================

``MUISPM_REGISTERPANEL EQU WM_USER+1760``

A custom windows message for the ModernUI_SmartPanel control that registers a dialog window (HWND) with the ModernUI_SmartPanel control 

**Parameters**

* **wParam** - Resource id of Dialog to register with the ModernUI_SmartPanel control
* **lParam** - Address of the Dialog's main procedure


**Return**

Returns handle of registered dialog ``HWND`` if successful, or ``NULL`` otherwise

**Example**

::

   InfoDialogProc PROTO :HWND, :UINT, :WPARAM, :LPARAM
   TestDialogProc PROTO :HWND, :UINT, :WPARAM, :LPARAM
   
   .const
   IDD_INFO_DIALOG EQU 2000 ; resource id assigned to dialog
   IDD_TEST_DIALOG EQU 3000 ; resource id assigned to dialog

::

   InfoDialogProc PROC hWin:HWND, uMsg:UINT, wParam:WPARAM, lParam:LPARAM
      mov eax, uMsg
      .IF eax == WM_INITDIALOG
   
      .ELSEIF eax == WM_COMMAND
   
      .ELSEIF eax==WM_CLOSE
         Invoke DestroyWindow, hWin
   
      .ELSE
         mov eax, FALSE
         ret
      .ENDIF
      mov eax, TRUE
      ret
   InfoDialogProc ENDP
   
   TestDialogProc PROC hWin:HWND, uMsg:UINT, wParam:WPARAM, lParam:LPARAM
      mov eax, uMsg
      .IF eax == WM_INITDIALOG
   
      .ELSEIF eax == WM_COMMAND
   
      .ELSEIF eax==WM_CLOSE
         Invoke DestroyWindow, hWin
   
      .ELSE
         mov eax, FALSE
         ret
      .ENDIF
      mov eax, TRUE
      ret
   TestDialogProc ENDP

::

   ; Register dialog panels with our Modern_SmartPanel control
   Invoke SendMessage, hSP, MUISPM_REGISTERPANEL, IDD_INFO_DIALOG, Addr InfoDialogProc
   Invoke SendMessage, hSP, MUISPM_REGISTERPANEL, IDD_TEST_DIALOG, Addr TestDialogProc
   
   Invoke SendMessage, hSP, MUISPM_SETCURRENTPANEL, 0, 0 ; set to first registered panel


**See Also**

:ref:`MUISPM_SETCURRENTPANEL<MUISPM_SETCURRENTPANEL>`, :ref:`MUISPM_GETCURRENTPANEL<MUISPM_GETCURRENTPANEL>` 

