.. _MUIAllocStructureMemory:

========================
MUIAllocStructureMemory 
========================

MUIAllocStructureMemory, PtrStructMem::ref:`POINTER<POINTER>`, TotalItems::ref:`MUIVALUE<MUIVALUE>`, ItemSize::ref:`MUIVALUE<MUIVALUE>`

Dynamically allocates (or reallocates) memory for a specified array of structures and auto increments the total items in the array, and returns a pointer to the new current item in the array of structures.

**Parameters**

* [in|out] **lpPtrStructMem** - pointer to variable used to store the pointer to the allocated structure
* [in] **TotalItems** - number of item elements currently in the structure
* [in] **ItemSize** - size of an item element in bytes

**Notes**

**lpPtrStructMem** is an address to receive the pointer to memory location of the base structure in memory. **lpPtrStructMem** can be ``NULL`` if **TotalItems** is ``0``, otherwise it must contain the address of the base structure in memory if the memory is to be increased (**TotalItems > 0**)

ItemSize is typically the ``SIZEOF`` structure to be allocated. This function calculates for you: *TotalItems * ItemSize*

If **lpPtrStructMem** is ``NULL`` then memory object is initialized to the size of *TotalItems * ItemSize* and the pointer to the memory allocated is returned

**Return**

Returns the pointer to the new structure item or ``-1`` if there was a problem allocating memory

**Example**

::
   
   ; Widget element
   Widget     STRUCT
     dwPrice  DD ?
     dwHeight DD ?
     dwWidth  DD ?
   Widge      ENDS
   
   ; pointers
   pMyWidgetArray DD 0
   pCurrentWidget DD 0
   
   ; Widget count
   dwTotalWidgets DD 0
	
::

   ; Assume dwTotalWidgets was previously set to 10 beforehand
   
   ; Add a new Widget to array of Widgets
   Invoke MUIAllocStructureMemory, Addr pMyWidgetArray, dwTotalWidgets, SIZEOF Widget
   .IF eax == -1
       ; Error - tell user?
       ret
   .ENDIF

   ; Save returned value as pointer to newly added element (Widget) in array
   mov pCurrentWidget, eax
   inc dwTotalWidgets ; update the total widgets count now
   
   ; total widgets will now be 11
   ; pCurrentWidget will point to this new 11th Widget

**See Also**

:ref:`MUIAllocMemProperties<MUIAllocMemProperties>`, :ref:`MUIFreeMemProperties<MUIFreeMemProperties>`

