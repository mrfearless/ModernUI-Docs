.. _MUIGetImageSize:

========================
MUIGetImageSize 
========================

MUIGetImageSize, hImage::ref:`MUIIMAGE<MUIIMAGE>`, ImageHandleType::ref:`MUIIT<MUIIT>`, lpImageWidth::ref:`LPMUIVALUE<LPMUIVALUE>`, lpImageHeight::ref:`LPMUIVALUE<LPMUIVALUE>`

Gets the image size of the specified image, based on the specified type: icon, bitmap or png. Width and Height are returned into the variables pointed to by the lpdwImageWidth and lpdwImageHeight parameters if successful.

**Parameters**

* [in] **hImage** - handle to image to get dimensions for
* [in] **ImageHandleType** - type of image used in **hImage**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [out] **lpImageWidth** - width of image
* [out] **lpImageHeight** - height of image

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUIGetImageSize, hMyBitmap, MUIIT_BMP, Addr dwWidth, Addr dwHeight

**See Also**

:ref:`MUIGetImageSizeEx<MUIGetImageSizeEx>`

