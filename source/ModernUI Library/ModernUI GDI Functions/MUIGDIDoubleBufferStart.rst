.. _MUIGDIDoubleBufferStart:

========================
MUIGDIDoubleBufferStart 
========================

**MUIGDIDoubleBufferStart, hWin:HWND, hdcSource:HDC, lpHDCBuffer:LPHANDLE, lpClientRect:LPRECT, lphBufferBitmap:LPHANDLE**

Starts double buffering. Used in a `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_ event. Place after `BeginPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-beginpaint.html>`_  call. **lpHDCBuffer** points to a variable used to store the ``HDC`` of the double buffer (eg. hdcMem). **lpClientRect** points to a ``RECT`` structure used to store the client rectangle. **lphBufferBitmap** points to a variable used to store the double buffer ``HBITMAP``.


**Parameters**

* [in] **hWin** - handle to the window to paint. Typically the control itself
* [in] **hdcSource** - the ``HDC`` source, typically the dc returned from the BeginPaint call
* [out] **lpHDCBuffer** - pointer to the variable used to store the double buffer ``HDC`` 
* [out] **lpClientRect** - pointer to the variable used to store the rectangle ``RECT`` of the window
* [out] **lphBufferBitmap** - pointer to the variable used to store the double buffer bitmap ``HBITMAP``

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   hdc:HDC 
   LOCAL hdcMem:HDC
   LOCAL hBufferBitmap:HBITMAP
   LOCAL rect:RECT

   Invoke BeginPaint, hWin, Addr ps
   mov hdc, eax

   Invoke MUIGDIDoubleBufferStart, hWin, hdc, Addr hdcMem, Addr rect, Addr hBufferBitmap 


**See Also**

:ref:`MUIGDIDoubleBufferFinish<MUIGDIDoubleBufferFinish>`, `BeginPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-beginpaint.html>`_, `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_, `EndPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-endpaint>`_

