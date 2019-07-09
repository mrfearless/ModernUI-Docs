.. _MUI_RGBCOLOR:

========================
MUI_RGBCOLOR Macro
========================

Creates a Red, Green, Blue ``COLORREF`` colour value used for **GDI** functions.

::

   MUI_RGBCOLOR MACRO red:REQ, green:REQ, blue:REQ
    EXITM < red or green shl 8 or blue shl 16 >
   ENDM


**Parameters**

* [in] **red** - ``0-255`` red color value
* [in] **green** - ``0-255`` green color value
* [in] **blue** - ``0-255`` blue color value

**Return**

Returns the RGB ``COLORREF`` value

**Example**

::

   mov BackColor, MUI_RGBCOLOR(127, 200, 240)

**See Also**

:ref:`RGB<RGB>`, :ref:`MUI_ARGBCOLOR<MUI_ARGBCOLOR>`

