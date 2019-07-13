.. _MUITextSetProperty:

========================
MUITextSetProperty 
========================

MUITextSetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`, PropertyValue::ref:`MUIPROPERTYVALUE<MUIPROPERTYVALUE>`

Sets the value of a property in the ModernUI_Text control. See :ref:`ModernUI_Text Properties<ModernUI_Text Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_Text control
* [in] **Property** - the property to set. See :ref:`ModernUI_Text Properties<ModernUI_Text Properties>` for details on the properties available
* [in] **PropertyValue** - the value to set the property to

**Return**

Returns the previously set value for the property, or ``NULL`` otherwise

**Example**

::

   Invoke MUITextSetProperty, hTxt1, @TextColor, MUI_RGBCOLOR(48,48,48)

**See Also**

:ref:`MUITextGetProperty<MUITextGetProperty>`, :ref:`ModernUI_Text Properties<ModernUI_Text Properties>`

