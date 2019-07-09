.. _MUIPaintBackgroundImage:

========================
MUIPaintBackgroundImage 
========================

Same as MUIPaintBackground, but with an image.

**MUIPaintBackgroundImage, hWin:HWND, Backcolor:COLORREF, BorderColor:COLORREF, hImage:HANDLE, ImageType:SIZE_T, ImageLocation:SIZE_T**

**Parameters**

* [in] **hWin** - handle to window to paint background for
* [in] **Backcolor** - color to paint background with
* [in] **BorderColor** - color to paint border with
* [in] **hImage** - handle to image to paint on background
* [in] **ImageType** - type of image used in **hImage**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [in] **ImageLocation** - location where to paint hImage: ``MUIIL_CENTER``, ``MUIIL_BOTTOMLEFT``, ``MUIIL_BOTTOMRIGHT``, ``MUIIL_TOPLEFT``, ``MUIIL_TOPRIGHT``, ``MUIIL_TOPCENTER``, or ``MUIIL_BOTTOMCENTER``

**Return**

None

**Notes**

You should handle the `WM_ERASEBKGND <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-erasebkgnd>`_ and `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_ events if you are going to use this function.

**Example**

::

   .ELSEIF eax == WM_ERASEBKGND
      mov eax, 1
      ret

   .ELSEIF eax == WM_PAINT
      Invoke MUIPaintBackgroundImage, hWin, MUI_RGBCOLOR(255,255,255), MUI_RGBCOLOR(48,48,48), hMyBitmap, MUIIT_BMP, MUIIL_CENTER
      mov eax, 0
      ret

**See Also**

:ref:`MUIPaintBackground<MUIPaintBackground>`, :ref:`MUI_RGBCOLOR<MUI_RGBCOLOR>`, `WM_ERASEBKGND <https://docs.microsoft.com/en-us/windows/win32/winmsg/wm-erasebkgnd>`_, `WM_PAINT <https://docs.microsoft.com/en-us/windows/win32/gdi/wm-paint>`_

