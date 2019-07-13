.. _MUISpinnerCreate:

========================
MUISpinnerCreate 
========================

MUISpinnerCreate, hWndParent::ref:`MUIWND<MUIWND>`, X::ref:`MUIVALUE<MUIVALUE>`, Y::ref:`MUIVALUE<MUIVALUE>`, nWidth::ref:`MUIVALUE<MUIVALUE>`, nHeight::ref:`MUIVALUE<MUIVALUE>`, ResourceID::ref:`RESID<RESID>`, Style::ref:`MUIVALUE<MUIVALUE>`

Creates a new ModernUI_Spinner control

**Parameters**

* [in] **hWndParent** - parent window of control
* [in] **X** - x coordinate of the control
* [in] **Y** - y coordinate of the control 
* [in] **nWidth** - width of the control
* [in] **nHeight** - height of the control
* [in] **ResourceID** - resource id of the control
* [in] **Style** - can be combination of style flags, see :ref:`ModernUI_Spinner Style Flags<ModernUI_Spinner Style Flags>` for details

**Return**

Returns handle to newly created ModernUI_Spinner control (``MUIWND``) if successful, or ``NULL`` otherwise

.. _ModernUI_Spinner Style Flags:

**ModernUI_Spinner Style Flags**

* ``MUISPNS_HAND`` - Show a hand instead of an arrow when mouse moves over spinner

**Example**

::

   Invoke MUISpinnerCreate, hWin, 100, 100, 64, 64, IDC_SPINNER, 0

**See Also**

:ref:`MUISpinnerRegister<MUISpinnerRegister>`, :ref:`MUISpinnerGetProperty<MUISpinnerGetProperty>`,  :ref:`MUISpinnerSetProperty<MUISpinnerSetProperty>`

