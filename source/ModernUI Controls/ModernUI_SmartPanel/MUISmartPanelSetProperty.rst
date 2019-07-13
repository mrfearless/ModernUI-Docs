.. _MUISmartPanelSetProperty:

========================
MUISmartPanelSetProperty 
========================

MUISmartPanelSetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`, PropertyValue::ref:`MUIPROPERTYVALUE<MUIPROPERTYVALUE>`

Sets the value of a property in a ModernUI_SmartPanel control. See :ref:`ModernUI_SmartPanel Properties<ModernUI_SmartPanel Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_SmartPanel control
* [in] **Property** - the property to set. See :ref:`ModernUI_SmartPanel Properties<ModernUI_SmartPanel Properties>` for details on the properties available
* [in] **PropertyValue** - the value to set the property to

**Return**

Returns the previously set value for the property, or ``NULL`` otherwise

**Example**

::

   Invoke MUISmartPanelSetProperty, hSP, @SmartPanelBackColor, MUI_RGBCOLOR(240,240,240)

**See Also**

:ref:`MUISmartPanelGetProperty<MUISmartPanelGetProperty>`, :ref:`ModernUI_SmartPanel Properties<ModernUI_SmartPanel Properties>`

