.. _MUISpinnerAddFrames:

========================
MUISpinnerAddFrames 
========================

MUISpinnerAddFrames, hWin::ref:`MUIWND<MUIWND>`, Count::ref:`MUIVALUE<MUIVALUE>`, ImageHandleType::ref:`MUIIT<MUIIT>`, lpArrayImageHandles::ref:`POINTER<POINTER>`

Process an array of image handles and add them to the spinner control as image frames

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **Count** - amount of handles in the array pointed to by **lpArrayImageHandles**
* [in] **ImageHandleType** - type of images used in array of handles **lpArrayImageHandles**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [in] **lpArrayImageHandles** - pointer to array of image handles

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISpinnerAddFrames, hSpinner, 10, MUI_PNG, Addr aPngHandles

**See Also**

:ref:`MUISpinnerAddFrame<MUISpinnerAddFrame>`, :ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>`, :ref:`MUISpinnerLoadFrames<MUISpinnerLoadFrames>`, :ref:`MUISpinnerLoadImage<MUISpinnerLoadImage>` 

