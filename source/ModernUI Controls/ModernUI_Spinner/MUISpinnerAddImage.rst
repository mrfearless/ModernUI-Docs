.. _MUISpinnerAddImage:

========================
MUISpinnerAddImage 
========================

MUISpinnerAddImage, hWin::ref:`MUIWND<MUIWND>`, hImage::ref:`GPIMAGE<GPIMAGE>`, NoFramesToCreate:::ref:`MUIVALUE<MUIVALUE>`, bReverse:BOOL

Add a single image (previously loaded), to rotate and create the animation frames for the spinner from. Note: **hImage** must be a **GDI+** image.

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **hImage** - handle to the image to add
* [in] **NoFramesToCreate** - no of frames to create from single image
* [in] **bReverse** - if ``TRUE`` reverses order of created frames

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISpinnerAddImage, pImageSpinCycle, 22, FALSE

**See Also**

:ref:`MUISpinnerLoadImage<MUISpinnerLoadImage>`, :ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>`, :ref:`MUISpinnerLoadFrames<MUISpinnerLoadFrames>`, :ref:`MUISpinnerAddFrame<MUISpinnerAddFrame>`, :ref:`MUISpinnerAddFrames<MUISpinnerAddFrames>`

