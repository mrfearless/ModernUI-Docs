.. _MUI_ARGBCOLOR:

========================
MUI_ARGBCOLOR Macro
========================

Creates an Alpha, Red, Green, Blue colour value used for **GDI+** functions.

::

   MUI_ARGBCOLOR MACRO alpha, red, green, blue
       EXITM < alpha SHL 24 OR red SHL 16 OR green SHL 8 OR blue >
   ENDM


**Parameters**

* [in] **alpha** - ``0-255`` alpha transparency value
* [in] **red** - ``0-255`` red color value
* [in] **green** - ``0-255`` green color value
* [in] **blue** - ``0-255`` blue color value

**Return**

Returns the ARGB value

**Example**

::

   mov BackColor, MUI_ARGBCOLOR(255, 127, 200, 240)

**See Also**

:ref:`AlphaRGB<AlphaRGB>`, :ref:`MUI_RGBCOLOR<MUI_RGBCOLOR>`

