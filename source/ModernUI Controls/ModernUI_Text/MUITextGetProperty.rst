.. _MUITextGetProperty:

========================
MUITextGetProperty 
========================

**MUITextGetProperty, hControl:DWORD, dwProperty:DWORD**

Get the value of a property in the ModernUI_Text control

**Parameters**

* [in] **hControl** - handle to the control
* [in] **dwProperty** - a constant, representing the property to get

**Return**

Returns the value of the property or ``NULL`` otherwise

**Example**

::

   LOCAL dwTextColor:DWORD
   
   Invoke MUITextGetProperty, hTxt1, @TextColor
   mov dwTextColor, eax

**See Also**

:ref:`MUITextSetProperty<MUITextSetProperty>`, :ref:`MUITextRegister<MUITextRegister>`, :ref:`MUITextCreate<MUITextCreate>`

