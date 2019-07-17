.. _MUISpinnerGetProperty:

========================
MUISpinnerGetProperty 
========================

MUISpinnerGetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`

Get the value of a property in a ModernUI_SmartPanel control. See :ref:`ModernUI_Spinner Properties<ModernUI_Spinner Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **Property** - the property to get. See :ref:`ModernUI_Spinner Properties<ModernUI_Spinner Properties>` for details on the properties available

**Return**

Returns the value of the property or ``NULL`` otherwise

**Example**

::

   LOCAL BackColor:DWORD
   
   Invoke MUISpinnerGetProperty, hSpinner, @SpinnerBackColor
   mov BackColor, eax

**See Also**

:ref:`MUISpinnerSetProperty<MUISpinnerSetProperty>`, :ref:`ModernUI_Spinner Properties<ModernUI_Spinner Properties>`

