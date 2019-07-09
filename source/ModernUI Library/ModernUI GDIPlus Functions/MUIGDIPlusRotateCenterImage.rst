.. _MUIGDIPlusRotateCenterImage:

===========================
MUIGDIPlusRotateCenterImage 
===========================

**MUIGDIPlusRotateCenterImage, hImage:HANDLE, fAngle:REAL4**

Rotates a **GDI+** image **hImage** around its center. **fAngle** is a ``REAL4`` value indicating the angle in degrees to rotate the original **hImage** by.

**Parameters**

* [in] **hImage** - handle to a GDI+ image to rotate
* [in] **fAngle** - degrees to rotate image


**Return**

Returns a new image handle of the rotated image

**Example**

::

   IFNDEF FP4
      FP4 MACRO value
      LOCAL vname
      .data
      align 4
        vname REAL4 value
      .code
      EXITM <vname>
      ENDM
   ENDIF

::

   Invoke MUIGDIPlusRotateCenterImage, pBitmap, FP4(45.0)

**See Also**

:ref:`MUIGDIPlusDoubleBufferStart<MUIGDIPlusDoubleBufferStart>`, :ref:`MUIGDIPlusDoubleBufferFinish<MUIGDIPlusDoubleBufferFinish>`

