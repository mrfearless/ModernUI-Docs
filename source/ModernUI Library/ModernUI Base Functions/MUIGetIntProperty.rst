.. _MUIGetIntProperty:

========================
MUIGetIntProperty 
========================

MUIGetIntProperty, hWin::ref:`MUIWND<MUIWND>`, Property::ref:`MUIPROPERTY<MUIPROPERTY>`

Get a specified property from the **internal** properties structure. Properties are defined as constants (eg ``@MyPropertyX EQU 4``) and are offsets into the memory location used to store the properties value. See :ref:`MUIAllocMemProperties<MUIAllocMemProperties>` for details on allocating memory for properties.

**Parameters**

* [in] **hWin** - handle to the ModernUI control
* [in] **Property** - The property to set

**Return**

Returns the property value or ``NULL``

**Example**


::

   .data
   ; Define internal properties
   @MyPropertyXcoord EQU 0
   @MyPropertyYcoord EQU 4
   @MyPropertyString EQU 8


::

   LOCAL dwX:DWORD
   LOCAL dwY:DWORD
   LOCAL lpszMyString:DWORD
   
   Invoke MUIGetIntProperty, hMyControl, @MyPropertyXcoord
   mov dwX, eax

   Invoke MUIGetIntProperty, hMyControl, @MyPropertyYcoord
   mov dwY, eax
   
   Invoke MUIGetIntProperty, hMyControl, @MyPropertyString
   mov lpszMyString, eax


**See Also**

:ref:`MUIAllocMemProperties<MUIAllocMemProperties>`, :ref:`MUISetIntProperty<MUISetIntProperty>`, :ref:`MUIGetExtProperty<MUIGetExtProperty>`, :ref:`MUISetExtProperty<MUISetExtProperty>`