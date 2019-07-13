.. _MUIGetImageSizeEx:

========================
MUIGetImageSizeEx 
========================

MUIGetImageSizeEx, hWin::ref:`MUIWND<MUIWND>`, hImage::ref:`MUIIMAGE<MUIIMAGE>`, ImageHandleType::ref:`MUIIT<MUIIT>`, lpImageWidth::ref:`LPMUIVALUE<LPMUIVALUE>`, lpImageHeight::ref:`LPMUIVALUE<LPMUIVALUE>`, lpImageX::ref:`LPMUIVALUE<LPMUIVALUE>`, lpImageY::ref:`LPMUIVALUE<LPMUIVALUE>`

Similar to MUIGetImageSize, but also returns centering x and y co-ordinate information based on rectangle of hWin


**Parameters**

* [in] **hWin** - handle to window to get center x and y coords for
* [in] **hImage** - handle to image to get dimensions for
* [in] **ImageHandleType** - type of image used in **hImage**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [out] **lpImageWidth** - width of image
* [out] **lpImageHeight** - height of image
* [out] **lpImageX** - x coord of image centered in hWin
* [out] **lpImageY** - y coord of image centered in hWin

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUIGetImageSizeEx, hWin, hMyBitmap, MUIIT_BMP, Addr dwWidth, Addr dwHeight, Addr xpos, Addr ypos

**See Also**

:ref:`MUIGetImageSize<MUIGetImageSize>`

