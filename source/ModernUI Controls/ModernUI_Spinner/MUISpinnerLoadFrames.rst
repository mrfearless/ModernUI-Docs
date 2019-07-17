.. _MUISpinnerLoadFrames:

========================
MUISpinnerLoadFrames 
========================

MUISpinnerLoadFrames, hWin::ref:`MUIWND<MUIWND>`, Count::ref:`MUIVALUE<MUIVALUE>`, ImageHandleType::ref:`MUIIT<MUIIT>`, lpArrayResourceIDs::ref:`POINTER<POINTER>`

Process an array of resource ids and load the resource and add them to the spinner control as image frames

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **Count** - amount of handles in the array pointed to by **lpArrayResourceIDs**
* [in] **ImageHandleType** - type of images used in array of resource ids **lpArrayResourceIDs**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [in] **lpArrayResourceIDs** - pointer to array of image resource ids

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISpinnerLoadFrames, hSpinner, 12, MUI_BMP, Addr aBitmapResources

**See Also**

:ref:`MUISpinnerAddFrame<MUISpinnerAddFrame>`, :ref:`MUISpinnerAddFrames<MUISpinnerAddFrames>`, :ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>`, :ref:`MUISpinnerLoadImage<MUISpinnerLoadImage>` 

