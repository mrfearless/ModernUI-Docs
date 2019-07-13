.. _MUISmartPanelRegisterPanel:

==========================
MUISmartPanelRegisterPanel 
==========================

MUISmartPanelRegisterPanel, hWin::ref:`MUIWND<MUIWND>`, ResIdPanelDlg::ref:`RESID<RESID>`, lpPanelProc::ref:`POINTER<POINTER>`

Registers a dialog panel to be used with the ModernUI_SmartPanel control. The dialogs are created by the ModernUI_SmartPanel control and are hidden until they are set to be active, by calls to :ref:`MUISmartPanelSetCurrentPanel<MUISmartPanelSetCurrentPanel>` or :ref:`MUISmartPanelNextPanel<MUISmartPanelNextPanel>` or :ref:`MUISmartPanelPrevPanel<MUISmartPanelPrevPanel>`.

**Parameters**

* [in] **hWin** - handle to the ModernUI_SmartPanel control
* [in] **ResIdPanelDlg** - resource id of dialog to register
* [in] **lpPanelProc** - address of dialog's main procedure

**Return**

Returns handle to newly created and registered panel ``MUIWND`` if successful, or ``NULL`` otherwise

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
   Invoke MUISmartPanelRegisterPanel, hSP, IDD_INFO_DIALOG, Addr InfoDialogProc
   Invoke MUISmartPanelRegisterPanel, hSP, IDD_TEST_DIALOG, Addr TestDialogProc
   
   Invoke MUISmartPanelSetCurrentPanel, hSP, 0 ; set to first registered panel

**See Also**

:ref:`MUISmartPanelSetIsDlgMsgVar<MUISmartPanelSetIsDlgMsgVar>`, :ref:`MUISmartPanelNextPanel<MUISmartPanelNextPanel>`, :ref:`MUISmartPanelPrevPanel<MUISmartPanelPrevPanel>`, :ref:`MUISmartPanelSetCurrentPanel<MUISmartPanelSetCurrentPanel>`

