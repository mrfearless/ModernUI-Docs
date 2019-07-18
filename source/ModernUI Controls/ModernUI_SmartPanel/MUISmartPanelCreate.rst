.. _MUISmartPanelCreate:

========================
MUISmartPanelCreate 
========================

MUISmartPanelCreate, hWndParent::ref:`MUIWND<MUIWND>`, X::ref:`MUIVALUE<MUIVALUE>`, Y::ref:`MUIVALUE<MUIVALUE>`, nWidth::ref:`MUIVALUE<MUIVALUE>`, nHeight::ref:`MUIVALUE<MUIVALUE>`, ResourceID::ref:`RESID<RESID>`, Style::ref:`MUIVALUE<MUIVALUE>`

Creates a new ModernUI_SmartPanel control

**Parameters**

* [in] **hWndParent** - parent window of control
* [in] **X** - x coordinate of the control
* [in] **Y** - y coordinate of the control 
* [in] **nWidth** - width of the control
* [in] **nHeight** - height of the control
* [in] **ResourceID** - resource id of the control
* [in] **Style** - can be combination of style flags, see :ref:`ModernUI_SmartPanel Style Flags<ModernUI_SmartPanel Style Flags>` for details

**Return**

Returns handle to newly created ModernUI_SmartPanel control (``MUIWND``) if successful, or ``NULL`` otherwise

.. _ModernUI_SmartPanel Style Flags:

**ModernUI_SmartPanel Style Flags**

* ``MUISPS_NORMAL`` - no slide animation
* ``MUISPS_NOSLIDE`` - no slide animation
* ``MUISPS_SLIDEPANELS_SLOW`` - slow speed slide animation
* ``MUISPS_SLIDEPANELS_NORMAL`` - normal speed slide animation
* ``MUISPS_SLIDEPANELS`` - normal speed slide animation
* ``MUISPS_SLIDEPANELS_FAST`` - fast speed slide animation
* ``MUISPS_SLIDEPANELS_VFAST`` - very fast speed slide animation
* ``MUISPS_SLIDEPANELS_INSTANT`` - no slide animation
* ``MUISPS_SPS_WRAPAROUND`` - for next/prev and showcase, if at end, moves to the right and starts again, otherwise if not specified, at last panel, scrolls left all the way back to start showing all panels along the way.
* ``MUISPS_SPS_SKIPBETWEEN`` - skips any in between panels, just moves from one to another.
* ``MUISPS_DESIGN_INFO`` - only used at design time to show text, which can be toggled off by user


**Example**

::

   Invoke MUISmartPanelCreate, hWin, 10, 10, 1024, 800, IDC_SMARTPANEL, MUISPS_NOSLIDE

**See Also**

:ref:`MUISmartPanelRegister<MUISmartPanelRegister>`, :ref:`MUISmartPanelGetProperty<MUISmartPanelGetProperty>`,  :ref:`MUISmartPanelSetProperty<MUISmartPanelSetProperty>`, :ref:`MUISmartPanelRegisterPanel<MUISmartPanelRegisterPanel>` 

