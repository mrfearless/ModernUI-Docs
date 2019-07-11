.. _MUITextRegister:

========================
MUITextRegister 
========================

**MUITextRegister**

Registers the window class for the ModernUI_Text control. This allows the control to be created via `CreateWindowEx <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-createwindowexa>`_ by specifying the class as '*ModernUI_Text*' and/or by the dialog manager when instantiating a new dialog with resources - if a custom control is using a class as '*ModernUI_Text*'.

**Parameters**

None

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUITextRegister

**See Also**

:ref:`MUITextCreate<MUITextCreate>`

