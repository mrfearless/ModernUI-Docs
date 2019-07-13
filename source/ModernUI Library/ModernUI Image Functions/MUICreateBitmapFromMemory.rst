.. _MUICreateBitmapFromMemory:

=========================
MUICreateBitmapFromMemory 
=========================

MUICreateBitmapFromMemory, pBitmapData::ref:`POINTER<POINTER>`

Create an bitmap from data stored in memory. Typically defined in the ``.data`` section as a variable with a sequence of binary data. Use bin2dbex from masm32 package to generate the byte sequence required. **pBitmapData** is a pointer to the bitmap file data.

**Parameters**

* [in] **pBitmapData** - pointer to the bitmap file data

**Return**

Returns a bitmap handle (``HBITMAP``) on success

**Example**

::
   
   .data
   BmpData db 66,77,58,0,0,0,0,0,0,0,54,0,0,0,40,0
           db 0,0,1,0,0,0,1,0,0,0,1,0,24,0,0,0
           db 0,0,0,0,0,0,194,30,0,0,194,30,0,0,0,0
           db 0,0,0,0,0,0,128,128,128,0

::
   
   LOCAL hBmp
   
   Invoke MUICreateBitmapFromMemory, Addr BmpData
   .IF eax == NULL
      ; error
   .ENDIF
   mov hBmp, eax
   

**See Also**

:ref:`MUICreateIconFromMemory<MUICreateIconFromMemory>`, :ref:`MUICreateCursorFromMemory<MUICreateCursorFromMemory>`

