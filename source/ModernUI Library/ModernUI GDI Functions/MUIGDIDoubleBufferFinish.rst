.. _MUIGDIDoubleBufferFinish:

========================
MUIGDIDoubleBufferFinish 
========================

MUIGDIDoubleBufferFinish, hdcBuffer:`HDC <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_, hBufferBitmap:`HBITMAP <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_, hBitmapUsed:`HBITMAP <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_, hFontUsed:`HFONT <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_, hBrushUsed:`HBRUSH <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_, hPenUsed:`HPEN <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_

Finishes double buffering and cleans up afterwards. Used in a `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_ event. Place before `EndPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-endpaint>`_ call and after all Blt (eg `BitBlt <https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-bitblt>`_) calls. **hdcBuffer** is the ``HDC`` of the double buffer (eg. hdcMem). **hBufferBitmap** is the handle to the double buffer bitmap. **hBitmapUsed**, **hFontUsed**, **hBrushUsed**, and **hPenUsed** are optional parameters. If you have used a bitmap image ``HBITMAP`` (not the double buffer bitmap which is **hBufferBitmap**) or a font ``HFONT``, brush ``HBRUSH`` or a pen ``HPEN`` in your code in the **hdcBuffer** you can pass the handles here for cleaning up, otherwise pass ``NULL`` or ``0`` for those other parameters.

**Parameters**

* [in] **hdcBuffer** - the double buffer dc (eg hdcMem)
* [in] **hBufferBitmap** - the double buffer bitmap ``HBITMAP``
* [in] **hBitmapUsed** - optional ``HBITMAP`` used in double buffer dc
* [in] **hFontUsed** - optional handle to a ``HFONT`` used in double buffer dc
* [in] **hBrushUsed** - optional handle to a ``HBRUSH`` used in double buffer dc
* [in] **hPenUsed** - optional handle to a ``HPEN`` used in double buffer dc

**Return**

None

**Example**

::

   Invoke BitBlt, hdc, 0, 0, rect.right, rect.bottom, hdcMem, 0, 0, SRCCOPY
 
   Invoke MUIGDIDoubleBufferFinish, hdcMem, hBufferBitmap, 0, 0, hBrush, 0

   Invoke EndPaint, hWin, Addr ps


**See Also**

:ref:`MUIGDIDoubleBufferStart<MUIGDIDoubleBufferStart>`, `BeginPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-beginpaint.html>`_, `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_, `EndPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-endpaint>`_

