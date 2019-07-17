.. _MUISpinnerLoadFrame:

========================
MUISpinnerLoadFrame 
========================

MUISpinnerLoadFrame, hWin::ref:`MUIWND<MUIWND>`, ImageHandleType::ref:`MUIIT<MUIIT>`, idResImage::ref:`RESID<RESID>`

Loads a resource as an image frame to the spinner control

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **ImageHandleType** - type of image to load in **idResImage**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [in] **idResImage** - resource id of image to load

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISpinnerLoadFrame, hSpinner, MUI_BMP, BMP_TESTER

**See Also**

:ref:`MUISpinnerAddFrames<MUISpinnerAddFrames>`, :ref:`MUISpinnerAddFrames<MUISpinnerAddFrames>`, :ref:`MUISpinnerLoadFrames<MUISpinnerLoadFrames>`, :ref:`MUISpinnerLoadImage<MUISpinnerLoadImage>` 

