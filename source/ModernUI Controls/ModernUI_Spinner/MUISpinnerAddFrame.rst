.. _MUISpinnerAddFrame:

========================
MUISpinnerAddFrame 
========================

MUISpinnerAddFrame, hWin::ref:`MUIWND<MUIWND>`, ImageHandleType::ref:`MUIIT<MUIIT>`, hImage::ref:`MUIIMAGE<MUIIMAGE>`

Adds an image frame to the spinner control

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **ImageHandleType** - type of image used in **hImage**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [in] **hImage** - handle to image

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISpinnerAddFrame, hSpinner, MUI_PNG, pPngImage

**See Also**

:ref:`MUISpinnerAddFrames<MUISpinnerAddFrames>`, :ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>`, :ref:`MUISpinnerLoadFrames<MUISpinnerLoadFrames>`, :ref:`MUISpinnerLoadImage<MUISpinnerLoadImage>` 

