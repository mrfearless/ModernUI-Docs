.. _MUIProgressBarGetProperty:

=========================
MUIProgressBarGetProperty 
=========================

MUIProgressBarGetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`

Get the value of a property in a ModernUI_ProgressBar control. See :ref:`ModernUI_ProgressBar Properties<ModernUI_ProgressBar Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_ProgressBar control
* [in] **Property** - the property to get. See :ref:`ModernUI_ProgressBar Properties<ModernUI_ProgressBar Properties>` for details on the properties available

**Return**

Returns the value of the property or ``NULL`` otherwise

**Example**

::

   LOCAL ProgressColor:DWORD
   
   Invoke MUIProgressBarGetProperty, hProgressBar, @ProgressBarProgressColor
   mov ProgressColor, eax

**See Also**

:ref:`MUIProgressBarSetProperty<MUIProgressBarSetProperty>`, :ref:`ModernUI_ProgressBar Properties<ModernUI_ProgressBar Properties>`