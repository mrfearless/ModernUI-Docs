.. _MUIButtonSetProperty:

========================
MUIButtonSetProperty 
========================

MUIButtonSetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`, PropertyValue::ref:`MUIPROPERTYVALUE<MUIPROPERTYVALUE>`

Sets the value of a property in a ModernUI_Button control. See :ref:`ModernUI_Button Properties<ModernUI_Button Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_Button control
* [in] **Property** - the property to set. See :ref:`ModernUI_Button Properties<ModernUI_Button Properties>` for details on the properties available
* [in] **PropertyValue** - the value to set the property to

**Return**

Returns the previously set value for the property, or ``NULL`` otherwise

**Example**

::

   Invoke MUIButtonSetProperty, hTxt1, @ButtonTextColor, MUI_RGBCOLOR(48,48,48)

**See Also**

:ref:`MUIButtonGetProperty<MUIButtonGetProperty>`, :ref:`ModernUI_Button Properties<ModernUI_Button Properties>`

