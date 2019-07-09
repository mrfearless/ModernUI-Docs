.. _MUIGDIPaintFrame:

========================
MUIGDIPaintFrame
========================

**MUIGDIPaintFrame, hdc:HDC, lpFrameRect:LPRECT, FrameColor:COLORREF, FrameStyle:SIZE_T**

Draws a border (or parts of) around a rectangle, as specified by the **lpFrameRect** parameter which points to a ``RECT``, with **FrameColor** which is a specific ``COLORREF`` color, to a ``HDC`` as specified by **hdc**.


**Parameters**

* [in] **hdc** - dc to paint the frame to
* [in] **lpFrameRect** - points to a ``RECT`` that defines area to paint the frame
* [in] **FrameColor** - color to paint the frame edges
* [in] **FrameStyle** - indicates what parts of the frame are painted. **FrameStyle** can be a combination of the following flags: ``MUIPFS_NONE``, ``MUIPFS_LEFT``, ``MUIPFS_TOP``, ``MUIPFS_BOTTOM``, ``MUIPFS_RIGHT`` or ``MUIPFS_ALL``


**Return**

None

**Example**

::

   LOCAL rect:RECT
   LOCAL BorderColor:COLORREF
   
   Invoke GetClientRect, hWin, Addr rect
   mov BorderColor, MUI_RGBCOLOR(127, 200, 240)
   
   Invoke MUIGDIPaintFrame, hdc, Addr rect, BorderColor, MUIPFS_ALL

**See Also**

:ref:`MUIGDIPaintFill<MUIGDIPaintFill>`, :ref:`MUI_RGBCOLOR<MUI_RGBCOLOR>`

