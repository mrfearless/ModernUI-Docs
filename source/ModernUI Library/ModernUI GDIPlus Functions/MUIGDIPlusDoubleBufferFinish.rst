.. _MUIGDIPlusDoubleBufferFinish:

============================
MUIGDIPlusDoubleBufferFinish 
============================

MUIGDIPlusDoubleBufferFinish, hWin::ref:`MUIWND<MUIWND>`, pGraphics::ref:`GPGRAPHICS<GPGRAPHICS>`, pBitmap::ref:`GPIMAGE<GPIMAGE>`, pGraphicsBuffer::ref:`GPGRAPHICS<GPGRAPHICS>`

Finish Double Buffering for **GDI+** & copy finished pGraphicsBuffer to pGraphics (HDC). Used in a `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_ event. Place before `EndPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-endpaint>`_

**Parameters**

* [in] **hWin** - handle to window that has double buffering (gdi+)
* [in] **pGraphics** - graphics context for the **hWin** window
* [in] **hBitmap** - double buffer image
* [in] **pGraphicsBuffer** - double buffer graphics context

**Return**

None

**Example**

::

   LOCAL hdc:HDC
   LOCAL pGraphics:DWORD
   LOCAL pGraphicsBuffer:DWORD
   LOCAL pBitmap:DWORD

   Invoke BeginPaint, hWin, Addr ps
   mov hdc, eax
   
   mov pGraphics, 0
   mov pGraphicsBuffer, 0
   mov pBitmap, 0
   
   Invoke GdipCreateFromHDC, hdc, Addr pGraphics
   
   ; Start GDI+ Double Buffer
   Invoke MUIGDIPlusDoubleBufferStart, hWin, pGraphics, Addr pBitmap, Addr pGraphicsBuffer
   
   ; Draw with GDI+ to pGraphicsBuffer context
   
   ; Finish GDI+ Double Buffer
   Invoke MUIGDIPlusDoubleBufferFinish, hWin, pGraphics, pBitmap, pGraphicsBuffer 
   
   .IF pGraphics != 0
      Invoke GdipDeleteGraphics, pGraphics
   .ENDIF
   
   Invoke EndPaint, hWin, Addr ps

**See Also**

:ref:`MUIGDIPlusDoubleBufferStart<MUIGDIPlusDoubleBufferStart>`, `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_, `EndPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-endpaint>`_

