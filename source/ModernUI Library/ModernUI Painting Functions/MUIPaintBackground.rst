.. _MUIPaintBackground:

========================
MUIPaintBackground 
========================

MUIPaintBackground, hWin::ref:`MUIWND<MUIWND>`, Backcolor::ref:`MUICOLORRGB<MUICOLORRGB>`, BorderColor::ref:`MUICOLORRGB<MUICOLORRGB>`

Paint the background of the a window a specified ``COLORREF`` color. Optionally provide **BorderColor** for a border ``COLORREF`` color to draw. If **BorderColor** = 0, no border is drawn. If you require black for border, use ``1``, or ``MUI_RGBCOLOR(1,1,1)``

**Parameters**

* [in] **hWin** - handle to window to paint background for
* [in] **Backcolor** - color to paint background with
* [in] **BorderColor** - color to paint border with


**Return**

None

**Notes**

You should handle the `WM_ERASEBKGND <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-erasebkgnd>`_ and `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_ events if you are going to use this function.

If you are using this on a window/dialog that does not use the ModernUI_CaptionBar control AND window/dialog is resizeable, you should place a call to `InvalidateRect <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-invalidaterect>`_ in the `WM_NCCALCSIZE <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-nccalcsize>`_ handler to prevent ugly drawing artefacts when border is drawn whilst resize of window/dialog occurs.

The ModernUI_CaptionBar handles this call to `WM_NCCALCSIZE <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-nccalcsize>`_ already by default

Here is an example of what to include if you need:

::

   .ELSEIF eax == WM_NCCALCSIZE
      Invoke InvalidateRect, hWin, NULL, TRUE


**Example**

::

   .ELSEIF eax == WM_ERASEBKGND
      mov eax, 1
      ret

   .ELSEIF eax == WM_PAINT
      Invoke MUIPaintBackground, hWin, MUI_RGBCOLOR(255,255,255), MUI_RGBCOLOR(48,48,48)
      mov eax, 0
      ret
		
**See Also**

:ref:`MUIPaintBackgroundImage<MUIPaintBackgroundImage>`, :ref:`MUI_RGBCOLOR<MUI_RGBCOLOR>`, `WM_ERASEBKGND <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-erasebkgnd>`_, `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_, `WM_NCCALCSIZE <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-nccalcsize>`_, `InvalidateRect <https://docs.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-invalidaterect>`_

