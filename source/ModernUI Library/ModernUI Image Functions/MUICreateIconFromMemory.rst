.. _MUICreateIconFromMemory:

========================
MUICreateIconFromMemory 
========================

MUICreateIconFromMemory, pIconData::ref:`POINTER<POINTER>`, iIcon::ref:`MUIVALUE<MUIVALUE>`

Create an icon from data stored in memory. Typically defined in the ``.data`` section as a variable with a sequence of binary data. Use bin2dbex from masm32 package to generate the byte sequence required. **pIconData** is a pointer to the icon file data.


**Parameters**

* [in] **pIconData** - pointer to the icon file data
* [in] **iIcon** - set to 0

**Return**

Returns an icon handle (``HICON``) on success

**Example**

::
   
   .data
   IconData db 0,0,1,0,1,0,1,1,0,0,1,0,24,0,48,0
            db 0,0,22,0,0,0,40,0,0,0,1,0,0,0,2,0
            db 0,0,1,0,24,0,0,0,0,0,8,0,0,0,0,0
            db 0,0,0,0,0,0,0,0,0,0,0,0,0,0,128,128
            db 128,11,0,0,0,0

::
   
   LOCAL hIco
   
   Invoke MUICreateIconFromMemory, Addr IconData, 0
   .IF eax == NULL
      ; error
   .ENDIF
   mov hIco, eax

**See Also**

:ref:`MUICreateBitmapFromMemory<MUICreateBitmapFromMemory>`, :ref:`MUICreateCursorFromMemory<MUICreateCursorFromMemory>`

