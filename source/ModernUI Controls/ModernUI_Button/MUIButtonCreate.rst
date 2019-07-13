.. _MUIButtonCreate:

========================
MUIButtonCreate 
========================

MUIButtonCreate, hWndParent::ref:`MUIWND<MUIWND>`, lpszText:LPSTR, X::ref:`MUIVALUE<MUIVALUE>`, Y::ref:`MUIVALUE<MUIVALUE>`, nWidth::ref:`MUIVALUE<MUIVALUE>`, nHeight::ref:`MUIVALUE<MUIVALUE>`, ResourceID::ref:`RESID<RESID>`, Style::ref:`MUIVALUE<MUIVALUE>`

Creates a new ModernUI_Button control.

**Parameters**

* [in] **hWndParent** - parent window of control
* [in] **lpszText** - text to display
* [in] **X** - x coord of control
* [in] **Y** - y coord of control
* [in] **nWidth** - width of control
* [in] **nHeight** - height of control
* [in] **ResourceID** - resource id of control
* [in] **Style** - can be combination of style flags, see :ref:`ModernUI_Button Style Flags<ModernUI_Button Style Flags>` for details

**Return**

Returns handle to newly created ModernUI_Button control (``MUIWND``) if successful, or ``NULL`` otherwise

.. _ModernUI_Button Style Flags:

**ModernUI_Button Style Flags**

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

:ref:`MUIButtonRegister<MUIButtonRegister>`, :ref:`MUIButtonGetProperty<MUIButtonGetProperty>`,  :ref:`MUIButtonSetProperty<MUIButtonSetProperty>`

