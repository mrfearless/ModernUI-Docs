.. _MUIGDIPlusPaintFrameI:

========================
MUIGDIPlusPaintFrameI
========================

**MUIGDIPlusPaintFrameI, pGraphics:HANDLE, lpFrameRectI:LPRECT, FrameColor:SIZE_T, FrameStyle:SIZE_T**

Draws a border (or parts of) around a rectangle, as specified by the **lpFrameRectI** parameter which points to a ``RECT``, with **FrameColor** which is a specific ARGB color, to a graphics context as specified by **pGraphics**.


**Parameters**

* [in] **pGraphics** - graphics context to paint the frame to
* [in] **lpFrameRectI** - points to a ``RECT`` that defines area to paint the frame
* [in] **FrameColor** - color to paint the frame edges
* [in] **FrameStyle** - indicates what parts of the frame are painted. **FrameStyle** can be a combination of the following flags: ``MUIPFS_NONE``, ``MUIPFS_LEFT``, ``MUIPFS_TOP``, ``MUIPFS_BOTTOM``, ``MUIPFS_RIGHT`` or ``MUIPFS_ALL``


**Return**

None

**Example**

::

   LOCAL hdc:HDC
   LOCAL pGraphics:DWORD
   LOCAL rect:RECT
   LOCAL BorderColor:DWORD

   Invoke BeginPaint, hWin, Addr ps
   mov hdc, eax
   
   mov pGraphics, 0
   Invoke GdipCreateFromHDC, hdc, Addr pGraphics
   
   Invoke GetClientRect, hWin, Addr rect
   mov BorderColor, MUI_ARGBCOLOR(255, 48, 48, 48)
   
   Invoke MUIGDIPlusPaintFrameI, pGraphics, Addr rect, BorderColor, MUIPFS_ALL

**See Also**

:ref:`MUIGDIPlusPaintFrame<MUIGDIPlusPaintFrame>`, :ref:`MUIGDIPlusPaintFillI<MUIGDIPlusPaintFillI>`, :ref:`MUIGDIPlusPaintFill<MUIGDIPlusPaintFill>`, :ref:`MUI_ARGBCOLOR<MUI_ARGBCOLOR>`

