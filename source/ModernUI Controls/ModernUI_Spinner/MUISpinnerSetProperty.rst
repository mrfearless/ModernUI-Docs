.. _MUISpinnerSetProperty:

========================
MUISpinnerSetProperty 
========================

MUISpinnerSetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`, PropertyValue::ref:`MUIPROPERTYVALUE<MUIPROPERTYVALUE>`

Sets the value of a property in a ModernUI_Spinner control. See :ref:`ModernUI_Spinner Properties<ModernUI_Spinner Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **Property** - the property to set. See :ref:`ModernUI_Spinner Properties<ModernUI_Spinner Properties>` for details on the properties available
* [in] **PropertyValue** - the value to set the property to

**Return**

Returns the previously set value for the property, or ``NULL`` otherwise

**Example**

::

   Invoke MUISpinnerSetProperty, hSpinner, @SpinnerBackColor, MUI_RGBCOLOR(240,240,240)

**See Also**

:ref:`MUISpinnerGetProperty<MUISpinnerGetProperty>`, :ref:`ModernUI_Spinner Properties<ModernUI_Spinner Properties>`

