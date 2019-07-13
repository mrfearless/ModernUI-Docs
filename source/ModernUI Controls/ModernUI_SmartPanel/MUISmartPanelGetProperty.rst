.. _MUISmartPanelGetProperty:

========================
MUISmartPanelGetProperty 
========================

MUISmartPanelGetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`

Get the value of a property in a ModernUI_SmartPanel control. See :ref:`ModernUI_SmartPanel Properties<ModernUI_SmartPanel Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_SmartPanel control
* [in] **Property** - the property to get. See :ref:`ModernUI_SmartPanel Properties<ModernUI_SmartPanel Properties>` for details on the properties available

**Return**

Returns the value of the property or ``NULL`` otherwise

**Example**

::

   LOCAL BackColor:DWORD
   
   Invoke MUISmartPanelGetProperty, hSP, @SmartPanelBackColor
   mov BackColor, eax

**See Also**

:ref:`MUISmartPanelSetProperty<MUISmartPanelSetProperty>`, :ref:`ModernUI_SmartPanel Properties<ModernUI_SmartPanel Properties>`

