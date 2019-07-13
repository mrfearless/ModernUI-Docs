.. _MUIGDIPlusPaintFill:

========================
MUIGDIPlusPaintFill 
========================

MUIGDIPlusPaintFill, pGraphics::ref:`GPGRAPHICS<GPGRAPHICS>`, lpFillGdipRect::ref:`LPGPRECT<LPGPRECT>`, FillColor::ref:`MUICOLORARGB<MUICOLORARGB>`

Fills a rectangle, as specified by the **lpFillRect** parameter which points to a ``GDIPRECT``, with **FillColor** which is a specific ARGB color, to a graphics context as specified by **pGraphics**. Note: a ``RECT`` can be converted to the :ref:`GDIPRECT<GDIPRECT>` using the :ref:`MUIGDIPlusRectToGdipRect<MUIGDIPlusRectToGdipRect>` function.


**Parameters**

* [in] **pGraphics** - graphics context to paint the filled rectangle to
* [in] **lpFillRect** - points to a ``GDIPRECT`` that defines area to paint fill
* [in] **FillColor** - ARGB color to paint fill


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

   LOCAL hdc:HDC
   LOCAL pGraphics:DWORD
   LOCAL rect:RECT
   LOCAL gdiprect:GDIPRECT
   LOCAL BackColor:DWORD

   Invoke BeginPaint, hWin, Addr ps
   mov hdc, eax
   
   mov pGraphics, 0
   Invoke GdipCreateFromHDC, hdc, Addr pGraphics
   
   Invoke GetClientRect, hWin, Addr rect
   Invoke MUIGDIPlusRectToGdipRect, Addr rect, Addr gdiprect
   
   mov BackColor, MUI_ARGBCOLOR(255, 127, 200, 240)
   
   Invoke MUIGDIPlusPaintFill, pGraphics, Addr gdiprect, BackColor

**See Also**

:ref:`MUIGDIPlusPaintFillI<MUIGDIPlusPaintFillI>`, :ref:`MUIGDIPlusPaintFrame<MUIGDIPlusPaintFrame>`, :ref:`MUIGDIPlusPaintFrameI<MUIGDIPlusPaintFrameI>`, :ref:`MUI_ARGBCOLOR<MUI_ARGBCOLOR>`, :ref:`MUIGDIPlusRectToGdipRect<MUIGDIPlusRectToGdipRect>`, :ref:`GDIPRECT<GDIPRECT>`

