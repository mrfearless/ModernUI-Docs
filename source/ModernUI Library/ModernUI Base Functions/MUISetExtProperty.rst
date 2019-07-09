.. _MUISetExtProperty:

========================
MUISetExtProperty 
========================

**MUISetExtProperty, hControl:HWND, Property:SIZE_T, PropertyValue:SIZE_T**

Sets a specified property in the **external** properties structure. Properties are defined as constants (eg ``@MyPropertyX EQU 4``) and are offsets into the memory location used to store the properties value. See :ref:`MUIAllocMemProperties<MUIAllocMemProperties>` for details on allocating memory for properties.

**Parameters**

* [in] **hControl** - handle to the ModernUI control
* [in] **Property** - The property to set
* [in] **PropertyValue** - The value to set the property to

**Return**

Returns the previously set property value or ``NULL``

**Example**

::

   .data
   MyString db 'test',0
   
   ; Define external properties
   @MyPropertyXcoord EQU 0
   @MyPropertyYcoord EQU 4
   @MyPropertyString EQU 8

::

   LOCAL dwX:DWORD
   LOCAL dwY:DWORD
   
   mov dwX, 1234
   Invoke MUISetExtProperty, hMyControl, @MyPropertyXcoord, dwX
   
   mov eax, 5678
   Invoke MUISetExtProperty, hMyControl, @MyPropertyYcoord, eax

   lea eax, MyString
   Invoke MUISetExtProperty, hMyControl, @MyPropertyString, eax


**See Also**

:ref:`MUIAllocMemProperties<MUIAllocMemProperties>`, :ref:`MUIGetExtProperty<MUIGetExtProperty>`, :ref:`MUIGetIntProperty<MUIGetIntProperty>`, :ref:`MUISetIntProperty<MUISetIntProperty>`

