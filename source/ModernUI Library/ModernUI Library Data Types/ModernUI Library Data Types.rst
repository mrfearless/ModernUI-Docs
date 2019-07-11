.. _ModernUI Library Data Types:

===========================
ModernUI Library Data Types
===========================

The following typedef or data types are used to help with documentation of ModernUI function parameters and return values, and with syncing ModernUI x86/x64 development by using one include file for both architectures: **ModernUI.inc**

-------------------
ModernUI Data Types
-------------------

These data types are specific to the ModernUI library:

+-------------------------------------------+--------------+--------------+
| **Data type**                             | **x86 size** | **x64 size** |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIWND<MUIWND>`                     | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIPROPERTIES<MUIPROPERTIES>`       | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIPROPERTY<MUIPROPERTY>`           | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIPROPERTYVALUE<MUIPROPERTYVALUE>` | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIVALUE<MUIVALUE>`                 | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`LPMUIVALUE<LPMUIVALUE>`             | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIIT<MUIIT>`                       | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIIL<MUIIL>`                       | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIPFS<MUIPFS>`                     | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUICOLORRGB<MUICOLORRGB>`           | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUICOLORARGB<MUICOLORARGB>`         | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`MUIIMAGE<MUIIMAGE>`                 | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+
| :ref:`LPMUIIMAGE<LPMUIIMAGE>`             | ``DWORD``    | ``QWORD``    |
+-------------------------------------------+--------------+--------------+

---------------
GDI+ Data Types
---------------

These data types expand on or add to some of the GDI+ data types:

+-----------------------------------+--------------+--------------+
| **Data type**                     | **x86 size** | **x64 size** |
+-----------------------------------+--------------+--------------+
| :ref:`GPGRAPHICS<GPGRAPHICS>`     | ``DWORD``    | ``QWORD``    |
+-----------------------------------+--------------+--------------+
| :ref:`LPGPGRAPHICS<LPGPGRAPHICS>` | ``DWORD``    | ``QWORD``    |
+-----------------------------------+--------------+--------------+
| :ref:`GPRECT<GPRECT>`             | ``DWORD``    | ``QWORD``    |
+-----------------------------------+--------------+--------------+
| :ref:`LPGPRECT<LPGPRECT>`         | ``DWORD``    | ``QWORD``    |
+-----------------------------------+--------------+--------------+
| :ref:`LPGDIPRECT<LPGDIPRECT>`     | ``DWORD``    | ``QWORD``    |
+-----------------------------------+--------------+--------------+
| :ref:`GPIMAGE<GPIMAGE>`           | ``DWORD``    | ``QWORD``    |
+-----------------------------------+--------------+--------------+
| :ref:`LPGPIMAGE<LPGPIMAGE>`       | ``DWORD``    | ``QWORD``    |
+-----------------------------------+--------------+--------------+


-----------------
Common Data Types
-----------------

These data types expand on or add to some of the common `Windows data types: <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_

+-----------------------------+--------------+--------------+
| **Data type**               | **x86 size** | **x64 size** |
+-----------------------------+--------------+--------------+
| :ref:`LPRECT<LPRECT>`       | ``DWORD``    | ``QWORD``    |
+-----------------------------+--------------+--------------+
| :ref:`LPHBITMAP<LPHBITMAP>` | ``DWORD``    | ``QWORD``    |
+-----------------------------+--------------+--------------+
| :ref:`LPHDC<LPHDC>`         | ``DWORD``    | ``QWORD``    |
+-----------------------------+--------------+--------------+
| :ref:`POINTER<POINTER>`     | ``DWORD``    | ``QWORD``    |
+-----------------------------+--------------+--------------+
| :ref:`RESID<RESID>`         | ``DWORD``    | ``QWORD``    |
+-----------------------------+--------------+--------------+


----------------------
Data Types Description
----------------------

.. _MUIWND:

**MUIWND**

Alias for `HWND <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_ window handle for a ModernUI control handle, typically defined as ``hWin``

.. _MUIPROPERTIES:

**MUIPROPERTIES**

Enum for cbWndExtraOffset parameter of :ref:`MUIAllocMemProperties<MUIAllocMemProperties>` and :ref:`MUIFreeMemProperties<MUIFreeMemProperties>` functions

.. _MUIPROPERTY:

**MUIPROPERTY**

Enum for a specific ModernUI Control's property, using the Property parameter of :ref:`MUIGetIntProperty<MUIGetIntProperty>`, :ref:`MUISetIntProperty<MUISetIntProperty>`, :ref:`MUIGetExtProperty<MUIGetExtProperty>` and :ref:`MUISetExtProperty<MUISetExtProperty>` functions

.. _MUIPROPERTYVALUE:

**MUIPROPERTYVALUE**

Value of specific ModernUI Control's property, using the PropertyValue parameter of :ref:`MUISetIntProperty<MUISetIntProperty>` or :ref:`MUISetExtProperty<MUISetExtProperty>` functions

.. _MUIVALUE:

**MUIVALUE**

A value, a constant or typically an unsigned integer used in certain ModernUI function parameters

.. _LPMUIVALUE:

**LPMUIVALUE**

A pointer to a :ref:`MUIVALUE<MUIVALUE>` value

.. _MUIIT:

**MUIIT**

Image type enum

.. _MUIIL:

**MUIIL**

Image location enum

.. _MUIPFS:

**MUIPFS**

Paint frame style enum for the FrameStyle parameter of the :ref:`MUIGDIPaintFrame<MUIGDIPaintFrame>` function

.. _MUICOLORRGB:

**MUICOLORRGB**

`COLORREF <https://docs.microsoft.com/en-us/windows/win32/gdi/colorref>`_ color value using :ref:`MUI_RGBCOLOR<MUI_RGBCOLOR>` macro

.. _MUICOLORARGB:

**MUICOLORARGB**

ARGB color value using :ref:`MUI_ARGBCOLOR<MUI_ARGBCOLOR>` macro

.. _MUIIMAGE:

**MUIIMAGE**

A bitmap (`HBITMAP <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_), icon (`HICON <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_) or a *GDI+* image (:ref:`GPIMAGE<GPIMAGE>`)

.. _LPMUIIMAGE:

**LPMUIIMAGE**

Pointer to a image (:ref:`MUIIMAGE<MUIIMAGE>`) handle

.. _GPGRAPHICS:

**GPGRAPHICS**

GDI+ graphics context

.. _LPGPGRAPHICS:

**LPGPGRAPHICS**

Pointer to a graphics context (:ref:`GPGRAPHICS<GPGRAPHICS>`) 

.. _GPRECT:

**GPRECT**

Alias for :ref:`GDIPRECT<GDIPRECT>`, a rectangle using REAL4 (float) for coordinates

.. _LPGPRECT:

**LPGPRECT**

Pointer to :ref:`GPRECT<GPRECT>`

.. _LPGDIPRECT:

**LPGDIPRECT**

Pointer to :ref:`GDIPRECT<GDIPRECT>`

.. _GPIMAGE:

**GPIMAGE**

A GDI+ image

.. _LPGPIMAGE:

**LPGPIMAGE**

Pointer to *GDI+* image (:ref:`GPIMAGE<GPIMAGE>`)

.. _LPRECT:

**LPRECT**

Pointer to `RECT <https://docs.microsoft.com/en-us/windows/win32/api/windef/ns-windef-rect>`_

.. _LPHBITMAP:

**LPHBITMAP**

Pointer to GDI bitmap (`HBITMAP <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_)

.. _LPHDC:

**LPHDC**

Pointer to `HDC <https://docs.microsoft.com/en-us/windows/win32/winprog/windows-data-types>`_

.. _POINTER:

**POINTER**

A pointer

.. _RESID:

**RESID**

A resource id value 
