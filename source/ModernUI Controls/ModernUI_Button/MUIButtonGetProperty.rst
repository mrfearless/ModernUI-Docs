.. _MUIButtonGetProperty:

========================
MUIButtonGetProperty 
========================

MUIButtonGetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`

Get the value of a property in a ModernUI_Button control. See :ref:`ModernUI_Button Properties<ModernUI_Button Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_Button control
* [in] **Property** - the property to get. See :ref:`ModernUI_Button Properties<ModernUI_Button Properties>` for details on the properties available

**Return**

Returns the value of the property or ``NULL`` otherwise

**Example**

::

   LOCAL dwTextColor:DWORD
   
   Invoke MUIButtonGetProperty, hTxt1, @ButtonTextColor
   mov dwTextColor, eax

**See Also**

:ref:`MUIButtonSetProperty<MUIButtonSetProperty>`, :ref:`ModernUI_Button Properties<ModernUI_Button Properties>`

