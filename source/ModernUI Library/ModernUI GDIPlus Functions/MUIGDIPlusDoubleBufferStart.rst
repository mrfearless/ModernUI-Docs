.. _MUIGDIPlusDoubleBufferStart:

===========================
MUIGDIPlusDoubleBufferStart 
===========================

MUIGDIPlusDoubleBufferStart, hWin::ref:`MUIWND<MUIWND>`, pGraphics::ref:`GPGRAPHICS<GPGRAPHICS>`, lpBitmapHandle::ref:`LPGPIMAGE<LPGPIMAGE>`, lpGraphicsBuffer::ref:`LPGPGRAPHICS<LPGPGRAPHICS>`

Start Double Buffering for **GDI+**. Used in a `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_ event. Place after `BeginPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-beginpaint.html>`_ 

**Parameters**

* [in] **hWin** - handle to window to start double buffering (gdi+) for
* [in] **pGraphics** - graphics context for the **hWin** window
* [out] **lpBitmapHandle** - pointer to variable to store double buffer image
* [out] **lpGraphicsBuffer** - pointer to variable to store double buffer graphics context

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

:ref:`MUIGDIPlusDoubleBufferFinish<MUIGDIPlusDoubleBufferFinish>`, `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_, `BeginPaint <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-beginpaint.html>`_

