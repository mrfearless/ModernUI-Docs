==========
Developers
==========

The following details information on ModernUI development, for those wishing to understand the conventions used and using ModernUI and ModernUI controls as a user or a developer.

**Functions/Procedures**

* **Public** functions should be prefixed with the ``MUI`` (ModernUI) abbreviation
* **Private** functions should be prefixed with ``_MUI_``

As a guideline, long code can be placed in their own procedure. Typically this might be for processing ``WM_`` messages (``WM_PAINT``) or where it helps readability.

**Variables**

Variables should be prefixed with Hungarian notation where possible

**Control Libraries**

* Control libraries should be prefixed with ``ModernUI_`` and then the name of the control.
* All controls should use there own include (.inc) file that has there own function prototypes, constants and global data variables (if applicable)
* The ModernUI.lib contains the main helper and utility functions for other MUI controls to use.
* The ModernUI.inc contains global constants used with the MUI framework.

**Use of ModernUI**

The inclusion of the ModernUI.inc and ModernUI.lib is required plus at a minimum one other control library and its own include file.

**Control Properties (Users)**

Properties can be changed (or read) by sending a custom message to the control via the standard `SendMessage <https://msdn.microsoft.com/en-us/library/windows/desktop/ms644950(v=vs.85).aspx>`_ Win32 api call.

Typically properties (defined the .inc include file of the control) that can be changed will relate to colours (text, background, border), fonts and other various attributes of the control.

To get property values for a control the ``MUI_GETPROPERTY`` message is used, ``wParam`` is set to the property to obtain.
To set property values for a control the ``MUI_SETPROPERTY`` message is used, ``wParam`` is set to the property to change, and ``lParam`` is set to the new property's value.

Example using an imaginary control that has a ``@TextColor`` property (defined in an include file) that allows the user to change the text color of the control:

::

   Invoke SendMessage, hModernUIControl, MUISETPROPERTY, @TextColor, 00FFFFFFh


Controls will also provide their own Get / Set functions for convenience that achieve the same results as sending the ``MUI_GETPROPERTY`` / ``MUI_SETPROPERTY`` messages.

The list of properties that can be accessed or changed will be stored in the .inc include file of the control.

**Control Properties (Developer Technical Notes)**

The ``cbWndExtra`` field of the `WNDCLASSEX <https://msdn.microsoft.com/en-us/library/windows/desktop/ms633577%28v=vs.85%29.aspx>`_ Structure  is used for storing pointers to two blocks of memory. One is for internal properties relating to the control, the second is for public exposed properties that can be set by the user. ``cbWndExtra`` should be set to ``8`` (``16`` *for ModernUI x64*) at a minimum to accommodate this when registering the new controls class.

Memory for both should be allocated during control creation (``WM_CREATE`` or ``WM_NCCREATE``) or after control creation, but before returning the control handle back to the user. 
The pointer to the block of memory for storing internal properties is stored at ``cbWndExtra +0`` and the pointer to the block of memory for storing external properties is stored at ``cbWndExtra +4`` (``cbWndExtra +8`` *for ModernUI x64*)

The helper function ``MUIAllocMemProperties`` is provided to easily allocate the memory required and store it in the appropriate ``cbWndExtra`` offset. Here is an example from the ModernUI_CaptionBar (x86) control:

::
	
	.ELSEIF eax == WM_CREATE
		Invoke _MUIAllocMemProperties, hWin, 0, SIZEOF _MUI_CAPTIONBAR_PROPERTIES ; internal properties
		Invoke _MUIAllocMemProperties, hWin, 4, SIZEOF MUI_CAPTIONBAR_PROPERTIES ; external properties
		Invoke _MUI_CaptionBarInit, hWin ; set some initial default property values
		mov eax, 0
		ret


Internal properties (to be changed by control developer) are defined as constant values which can be passed to the ``_MUIGetIntProperty`` / ``_MUISetIntProperty`` functions.

External properties (allowed to be changed by end-user) are defined as constant values which can be passed to the ``MUIGetExtProperty`` / ``MUISetExtProperty`` functions.

Controls should respond to the ``MUI_GETPROPERTY`` / ``MUI_SETPROPERTY`` messages, handling them with a forwarding call to ``MUIGetExtProperty`` / ``MUISetExtProperty`` functions and taking care of any other details as required.

Each control should also provide there own get / set property functions, which may just be wrappers for calls to the ``MUI_GETPROPERTY`` / ``MUI_SETPROPERTY`` messages. For controls that have other child controls that might be affected by a change to the parent's property value, this can be handled within ``MUI_GETPROPERTY`` / ``MUI_SETPROPERTY`` messages.

Each control should define there list of properties in their own include file for the user to reference.