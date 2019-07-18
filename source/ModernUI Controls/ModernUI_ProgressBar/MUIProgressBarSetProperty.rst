.. _MUIProgressBarSetProperty:

=========================
MUIProgressBarSetProperty 
=========================

MUIProgressBarSetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`, PropertyValue::ref:`MUIPROPERTYVALUE<MUIPROPERTYVALUE>`

Sets the value of a property in a ModernUI_ProgressBar control. See :ref:`ModernUI_ProgressBar Properties<ModernUI_ProgressBar Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_ProgressBar control
* [in] **Property** - the property to set. See :ref:`ModernUI_ProgressBar Properties<ModernUI_ProgressBar Properties>` for details on the properties available
* [in] **PropertyValue** - the value to set the property to

**Return**

Returns the previously set value for the property, or ``NULL`` otherwise

**Example**

::

   Invoke MUIProgressBarSetProperty, hProgressBar, @ProgressBarProgressColor, MUI_RGBCOLOR(67,104,210)

**See Also**

:ref:`MUIProgressBarGetProperty<MUIProgressBarGetProperty>`, :ref:`ModernUI_ProgressBar Properties<ModernUI_ProgressBar Properties>`
