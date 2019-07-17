.. _MUISpinnerLoadImage:

========================
MUISpinnerLoadImage 
========================

MUISpinnerLoadImage, hWin::ref:`MUIWND<MUIWND>`, idResImage::ref:`RESID<RESID>`, NoFramesToCreate:::ref:`MUIVALUE<MUIVALUE>`, bReverse:BOOL

Loads a single image from a resource, to rotate and create the animation frames for the spinner from. Note: **idResImage** must be a **PNG** stored in ``RC_DATA`` format

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **idResImage** - resource id of image to load
* [in] **NoFramesToCreate** - no of frames to create from single image
* [in] **bReverse** - if ``TRUE`` reverses order of created frames

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISpinnerLoadImage, hSpinner, PNG_SPINCYCLE, 22, FALSE

**See Also**

:ref:`MUISpinnerAddImage<MUISpinnerAddImage>`, :ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>`, :ref:`MUISpinnerLoadFrames<MUISpinnerLoadFrames>`, :ref:`MUISpinnerAddFrame<MUISpinnerAddFrame>`, :ref:`MUISpinnerAddFrames<MUISpinnerAddFrames>`

