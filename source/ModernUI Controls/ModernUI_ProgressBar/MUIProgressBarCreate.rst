.. _MUIProgressBarCreate:

========================
MUIProgressBarCreate 
========================

MUIProgressBarCreate, hWndParent::ref:`MUIWND<MUIWND>`, X::ref:`MUIVALUE<MUIVALUE>`, Y::ref:`MUIVALUE<MUIVALUE>`, nWidth::ref:`MUIVALUE<MUIVALUE>`, nHeight::ref:`MUIVALUE<MUIVALUE>`, ResourceID::ref:`RESID<RESID>`, Style::ref:`MUIVALUE<MUIVALUE>`

Creates a new ModernUI_ProgressBar control

**Parameters**

* [in] **hWndParent** - parent window of control
* [in] **X** - x coordinate of the control
* [in] **Y** - y coordinate of the control 
* [in] **nWidth** - width of the control
* [in] **nHeight** - height of the control
* [in] **ResourceID** - resource id of the control
* [in] **Style** - ``0``

**Return**

Returns handle to newly created ModernUI_SmartPanel control (``MUIWND``) if successful, or ``NULL`` otherwise

**Example**

::

   Invoke MUIProgressBarCreate, hWin, 100, 100, 300, 14, IDC_PBAR, 0

**See Also**

:ref:`MUIProgressBarRegister<MUIProgressBarRegister>`, :ref:`MUIProgressBarGetProperty<MUIProgressBarGetProperty>`,  :ref:`MUIProgressBarSetProperty<MUIProgressBarSetProperty>` 

