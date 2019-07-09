.. _MUIGDIPlusRectToGdipRect:

========================
MUIGDIPlusRectToGdipRect 
========================

**MUIGDIPlusRectToGdipRect, lpRect:LPRECT, lpGdipRect:LPGDIRECT**

Convert a ``RECT`` structure to a ``GDIPRECT`` structure.

**Parameters**

* [in] **lpRect** - pointer to ``RECT`` to convert
* [out] **lpGdipRect** - pointer to ``GDIRECT`` to store the result

**Return**

None

**Example**

::

   GDIPRECT     STRUCT
       left     REAL4 ?
       top      REAL4 ?
       right    REAL4 ?
       bottom   REAL4 ?
   GDIPRECT     ENDS

::

   LOCAL rect:RECT
   LOCAL gdirect:GDIRECT
   
   Invoke GetClientRect, hWin, Addr rect
   Invoke MUIGDIPlusRectToGdipRect, Addr rect, Addr gdirect

**See Also**

:ref:`MUIGDIPlusPaintFill<MUIGDIPlusPaintFill>`, :ref:`MUIGDIPlusPaintFrame<MUIGDIPlusPaintFrame>`

