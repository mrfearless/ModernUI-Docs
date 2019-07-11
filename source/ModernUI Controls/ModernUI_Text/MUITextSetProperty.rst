.. _MUITextSetProperty:

========================
MUITextSetProperty 
========================

**MUITextSetProperty, hControl:DWORD, dwProperty:DWORD, dwPropertyValue:DWORD**

Sets the value of a property in the ModernUI_Text control

**Parameters**

* [in] **hControl** - handle to the control
* [in] **dwProperty** - a constant, representing the property to set
* [in] **dwPropertyValue** - the value to set the property to

**Return**

Returns the previously set value of the property

**Example**

::

   Invoke MUITextSetProperty, hTxt1, @TextColor, MUI_RGBCOLOR(48,48,48)

**See Also**

:ref:`MUITextGetProperty<MUITextGetProperty>`, :ref:`MUITextRegister<MUITextRegister>`, :ref:`MUITextCreate<MUITextCreate>`

