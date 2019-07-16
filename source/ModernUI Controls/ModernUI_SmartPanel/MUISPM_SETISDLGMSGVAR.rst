.. _MUISPM_SETISDLGMSGVAR:

===================================
MUISPM_SETISDLGMSGVAR 
===================================

``MUISPM_SETISDLGMSGVAR EQU WM_USER+1754``

A custom windows message for the ModernUI_SmartPanel control that uses the variable pointed to by **wParam** to store the current panel handle of the ModernUI_SmartPanel control for use with `IsDialogMessage  <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-isdialogmessagea>`_ function

**Parameters**

* **wParam** - Address of variable to receive the current panel handle (``HWND``)
* **lParam** - ``NULL``


**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   .data
   dwCurrentPanelHandle DD 0 ; global variable to store current panel handle

::

   Invoke SendMessage, hSmartPanel, MUISPM_SETISDLGMSGVAR, Addr dwCurrentPanelHandle, NULL

**See Also**

:ref:`MUISmartPanelRegisterPanel<MUISmartPanelRegisterPanel>`

