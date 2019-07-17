.. _MUISpinnerAddSpriteSheet:

========================
MUISpinnerAddSpriteSheet 
========================

MUISpinnerAddSpriteSheet, hWin::ref:`MUIWND<MUIWND>`, SpriteCount::ref:`MUIVALUE<MUIVALUE>`, ImageHandleType::ref:`MUIIT<MUIIT>`, hImageSpriteSheet::ref:`MUIIMAGE<MUIIMAGE>`, bReverse:BOOL

Adds a long (wide) image strip from a previuosly loaded image, to use as the frames of the spinner animation. The width of each frame is calculated by dividing the length of the spritesheet image by **SpriteCount**

**Parameters**

* [in] **hWin** - handle to the ModernUI_Spinner control
* [in] **SpriteCount** - no of frames to split the spritesheet into
* [in] **ImageHandleType** - type of image used in **hImageSpriteSheet**: ``MUIIT_NONE``, ``MUIIT_BMP``, ``MUIIT_ICO``, or ``MUIIT_PNG``
* [in] **hImageSpriteSheet**
* [in] **bReverse** - if ``TRUE`` reverses order of created frames

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISpinnerAddSpriteSheet, hSpinner, 22, MUI_PNG, pImageSpriteSheet, FALSE

**See Also**

:ref:`MUISpinnerLoadSpriteSheet<MUISpinnerLoadSpriteSheet>`

