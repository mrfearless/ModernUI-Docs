.. _MUISmartPanelSetIsDlgMsgVar:

===========================
MUISmartPanelSetIsDlgMsgVar 
===========================

MUISmartPanelSetIsDlgMsgVar, hWin::ref:`MUIWND<MUIWND>`, lpVar::ref:`LPMUIVALUE<LPMUIVALUE>`

Specifies a variable that will used during a message event loop for use with `IsDialogMessage <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-isdialogmessagea>`_. **lpVar** points is an address of a variable that will hold the handle to the current dialog panel.

**Parameters**

* [in] **hWin** - handle to the ModernUI_SmartPanel control
* [out] **lpVar** - pointer to variable to store the current panel handle (``HWND``)

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   .data
   dwCurrentPanelHandle DD 0 ; global variable to store current panel handle

::

   Invoke MUISmartPanelSetIsDlgMsgVar, hSP1, Addr dwCurrentPanelHandle

**See Also**

:ref:`MUISmartPanelRegisterPanel<MUISmartPanelRegisterPanel>`

