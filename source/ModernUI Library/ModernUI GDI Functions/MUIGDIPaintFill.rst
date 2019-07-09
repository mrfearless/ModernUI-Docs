.. _MUIGDIPaintFill:

========================
MUIGDIPaintFill 
========================

**MUIGDIPaintFill, hdc:HDC, lpFillRect:LPRECT, FillColor:COLORREF**

Fills a rectangle, as specified by the **lpFillRect** parameter which points to a ``RECT``, with **FillColor** which is a specific ``COLORREF`` color, to a ``HDC`` as specified by **hdc**.


**Parameters**

* [in] **hdc** - dc to paint the filled rectangle to
* [in] **lpFillRect** - points to a ``RECT`` that defines area to paint fill
* [in] **FillColor** - color to paint fill


**Return**

None

**Example**

::

   LOCAL rect:RECT
   LOCAL BackColor:COLORREF
   
   Invoke GetClientRect, hWin, Addr rect
   mov BackColor, MUI_RGBCOLOR(127, 200, 240)
   
   Invoke MUIGDIPaintFill, hdc, Addr rect, BackColor

**See Also**

:ref:`MUIGDIPaintFrame<MUIGDIPaintFrame>`, :ref:`MUI_RGBCOLOR<MUI_RGBCOLOR>`

