.. _MUISPNM_ADDFRAME:

===================================
MUISPNM_ADDFRAME 
===================================

``MUISPNM_ADDFRAME EQU WM_USER+1752``

A custom windows message for the ModernUI_Spinner that adds an image handle (previously loaded) to the control

**Parameters**

* **wParam** - the spinner image type: ``MUISPIT_NONE``, ``MUISPIT_BMP``, ``MUISPIT_ICO`` or ``MUISPIT_PNG``
* **lParam** - handle to the image to add to the spinner


**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_ADDFRAME, MUISPIT_BMP, hBitmapImage

**See Also**

:ref:`MUISpinnerAddFrame<MUISpinnerAddFrame>`, :ref:`MUISPNM_LOADFRAME<MUISPNM_LOADFRAME>`, :ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>` 

