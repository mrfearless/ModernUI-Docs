.. _MUIGDIPlusPaintFillI:

========================
MUIGDIPlusPaintFillI 
========================

**MUIGDIPlusPaintFillI, pGraphics:HANDLE, lpFillRectI:LPRECT, FillColor:SIZE_T**

Fills a rectangle, as specified by the **lpFillRectI** parameter which points to a ``RECT``, with **FillColor** which is a specific ARGB color, to a graphics context as specified by **pGraphics**.


**Parameters**

* [in] **pGraphics** - graphics context to paint the filled rectangle to
* [in] **lpFillRectI** - points to a ``RECT`` that defines area to paint fill
* [in] **FillColor** - color to paint fill


**Return**

None

**Example**

::

   LOCAL hdc:HDC
   LOCAL pGraphics:DWORD
   LOCAL rect:RECT
   LOCAL BackColor:DWORD

   Invoke BeginPaint, hWin, Addr ps
   mov hdc, eax
   
   mov pGraphics, 0
   Invoke GdipCreateFromHDC, hdc, Addr pGraphics
   
   Invoke GetClientRect, hWin, Addr rect
   mov BackColor, MUI_ARGBCOLOR(255, 127, 200, 240)
   
   Invoke MUIGDIPlusPaintFillI, pGraphics, Addr rect, BackColor

**See Also**

:ref:`MUIGDIPlusPaintFill<MUIGDIPlusPaintFill>`, :ref:`MUIGDIPlusPaintFrameI<MUIGDIPlusPaintFrameI>`, :ref:`MUIGDIPlusPaintFrame<MUIGDIPlusPaintFrame>`, :ref:`MUI_ARGBCOLOR<MUI_ARGBCOLOR>`

