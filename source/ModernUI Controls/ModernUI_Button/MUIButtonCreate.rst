.. _MUIButtonCreate:

========================
MUIButtonCreate 
========================

**MUIButtonCreate, hWndParent:DWORD, lpszText:DWORD, xpos:DWORD, ypos:DWORD, controlwidth:DWORD, controlheight:DWORD, dwResourceID:DWORD, dwStyle:DWORD**

Creates a new ModernUI Button control.

**Parameters**

* [in] **hWndParent** - parent window of control
* [in] **lpszText** - text to display
* [in] **xpos** - x coord of control
* [in] **ypos** - y coord of control
* [in] **controlwidth** - width of control
* [in] **controlheight** - height of control
* [in] **dwResourceID** - resource id of control
* [in] **dwStyle** - can be combination of style flags, see notes for details

**Return**

Returns handle to newly created control if successful, or ``NULL`` otherwise

**Notes**

*dwStyle - style flags:*

* ``MUIBS_LEFT`` - Align text to the left of the button
* ``MUIBS_BOTTOM`` - Place image at the top, and text below
* ``MUIBS_CENTER`` - Align text centerally.
* ``MUIBS_AUTOSTATE`` - Automatically toggle between ``TRUE``/``FALSE`` state when clicked. ``TRUE`` = Selected.
* ``MUIBS_PUSHBUTTON`` - Simulate button movement down slightly when mouse click and movement up again when mouse is released.
* ``MUIBS_HAND`` - Show a hand instead of an arrow when mouse moves over button.
* ``MUIBS_KEEPIMAGES`` - Dont delete image handles when control is destoyed. Essential if image handles are used in multiple controls.
* ``MUIBS_DROPDOWN`` - Show dropdown arrow right side of control
* ``MUIBS_NOFOCUSRECT`` - Dont show focus rect, just use change border to ``@ButtonBorderColorAlt`` when setfocus.
* ``MUIBS_THEME`` - Use default windows theme colors and react to WM_THEMECHANGED


**Example**

::

   Invoke MUIButtonCreate, hWin, Addr szButtonText, 10, 10, 150, 30, IDC_BTN1, MUIBS_PUSHBUTTON or MUIBS_HAND

**See Also**

:ref:`MUIButtonRegister<MUIButtonRegister>`

