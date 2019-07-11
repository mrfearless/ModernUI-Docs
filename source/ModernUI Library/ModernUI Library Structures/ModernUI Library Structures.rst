.. ModernUI Library Structures:

===========================
ModernUI Library Structures
===========================

.. _GDIPRECT:

**GDIPRECT Structure:**

A rectangle structure that uses REAL4 (float) for coordinates instead of integers. This structure is used by certain **GDI+** functions that require float values.

::

   GDIPRECT     STRUCT
       left     REAL4 ?
       top      REAL4 ?
       right    REAL4 ?
       bottom   REAL4 ?
   GDIPRECT     ENDS


GDIPRECT Members
----------------

**left**

Specifies the x-coordinate of the upper-left corner of the rectangle.

**top**

Specifies the y-coordinate of the upper-left corner of the rectangle.

**right**

Specifies the x-coordinate of the lower-right corner of the rectangle.

**bottom**

Specifies the y-coordinate of the lower-right corner of the rectangle.