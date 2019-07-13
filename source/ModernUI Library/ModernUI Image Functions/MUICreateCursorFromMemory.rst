.. _MUICreateCursorFromMemory:

=========================
MUICreateCursorFromMemory 
=========================

MUICreateCursorFromMemory, pCursorData::ref:`POINTER<POINTER>`

Creates a cursor from icon/cursor data stored in memory. Typically defined in the ``.data`` section as a variable with a sequence of binary data. Use bin2dbex from masm32 package to generate the byte sequence required. **pCursorData** is a pointer to the cursor file data.

**Parameters**

* [in] **pCursorData**- pointer to the cursor file data


**Return**

Returns a cursor (a special animated icon) handle (``HICON``) on success

**Example**

::
   
   .data
   CursorData db 0,0,1,0,1,0,1,1,0,0,1,0,24,0,48,0
              db 0,0,22,0,0,0,40,0,0,0,1,0,0,0,2,0
              db 0,0,1,0,24,0,0,0,0,0,8,0,0,0,0,0
              db 0,0,0,0,0,0,0,0,0,0,0,0,0,0,128,128
              db 128,11,0,0,0,0

::
   
   LOCAL hCursor
   
   Invoke MUICreateCursorFromMemory, Addr CursorData
   .IF eax == NULL
      ; error
   .ENDIF
   mov hCursor, eax

**See Also**

:ref:`MUICreateBitmapFromMemory<MUICreateBitmapFromMemory>`, :ref:`MUICreateIconFromMemory<MUICreateIconFromMemory>`

