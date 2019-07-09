.. _MUIGDIPlusPaintFrame:

========================
MUIGDIPlusPaintFrame
========================

**MUIGDIPlusPaintFrame, pGraphics:HANDLE, lpFrameRect:LPGDIRECT, FrameColor:SIZE_T, FrameStyle:SIZE_T**

Draws a border (or parts of) around a rectangle, as specified by the **lpFrameRect** parameter which points to a ``GDIRECT``, with **FrameColor** which is a specific ARGB color, to a graphics context as specified by **pGraphics**. Note: a ``RECT`` can be converted to the ``GDIRECT`` using the :ref:`MUIGDIPlusRectToGdipRect<MUIGDIPlusRectToGdipRect>` function.


**Parameters**

* [in] **pGraphics** - graphics context to paint the frame to
* [in] **lpFrameRect** - points to a ``GDIRECT`` that defines area to paint the frame
* [in] **FrameColor** - color to paint the frame edges
* [in] **FrameStyle** - indicates what parts of the frame are painted. **FrameStyle** can be a combination of the following flags: ``MUIPFS_NONE``, ``MUIPFS_LEFT``, ``MUIPFS_TOP``, ``MUIPFS_BOTTOM``, ``MUIPFS_RIGHT`` or ``MUIPFS_ALL``


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
   LOCAL gdirect:GDIRECT
   LOCAL BorderColor:DWORD

   Invoke BeginPaint, hWin, Addr ps
   mov hdc, eax
   
   mov pGraphics, 0
   Invoke GdipCreateFromHDC, hdc, Addr pGraphics
   
   Invoke GetClientRect, hWin, Addr rect
   Invoke MUIGDIPlusRectToGdipRect, Addr rect, Addr gdirect
   
   mov BorderColor, MUI_ARGBCOLOR(255, 48, 48, 48)
   
   Invoke MUIGDIPlusPaintFrame, pGraphics, Addr gdirect, BorderColor, MUIPFS_ALL

**See Also**

:ref:`MUIGDIPlusPaintFrameI<MUIGDIPlusPaintFrameI>`, :ref:`MUIGDIPlusPaintFill<MUIGDIPlusPaintFill>`, :ref:`MUIGDIPlusPaintFillI<MUIGDIPlusPaintFillI>`, :ref:`MUI_ARGBCOLOR<MUI_ARGBCOLOR>`, :ref:`MUIGDIPlusRectToGdipRect<MUIGDIPlusRectToGdipRect>`

