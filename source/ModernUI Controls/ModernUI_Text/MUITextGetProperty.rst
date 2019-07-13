.. _MUITextGetProperty:

========================
MUITextGetProperty 
========================

MUITextGetProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`

Get the value of a property in the ModernUI_Text control. See :ref:`ModernUI_Text Properties<ModernUI_Text Properties>` for details on the properties available

**Parameters**

* [in] **hWin** - handle to the ModernUI_Text control
* [in] **Property** - the property to get. See :ref:`ModernUI_Text Properties<ModernUI_Text Properties>` for details on the properties available

**Return**

Returns the value of the property or ``NULL`` otherwise

**Example**

::

   LOCAL dwTextColor:DWORD
   
   Invoke MUITextGetProperty, hTxt1, @TextColor
   mov dwTextColor, eax

**See Also**

:ref:`MUITextSetProperty<MUITextSetProperty>`, :ref:`ModernUI_Text Properties<ModernUI_Text Properties>`

