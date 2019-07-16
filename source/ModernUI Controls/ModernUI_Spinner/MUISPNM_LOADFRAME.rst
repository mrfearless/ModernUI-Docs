.. _MUISPNM_LOADFRAME:

===================================
MUISPNM_LOADFRAME 
===================================

``MUISPNM_LOADFRAME EQU WM_USER+1751``

A custom windows message for the ModernUI_Spinner that loads an image from a resource and adds to the ModernUI_Spinner control

**Parameters**

* **wParam** - the spinner image type: ``MUISPIT_NONE``, ``MUISPIT_BMP``, ``MUISPIT_ICO`` or ``MUISPIT_PNG``
* **lParam** - resource id of the image to load and add to the spinner


**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_LOADFRAME, MUISPIT_PNG, pPngImage

**See Also**

:ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>`, :ref:`MUISPNM_ADDFRAME<MUISPNM_ADDFRAME>`, :ref:`MUISpinnerAddFrame<MUISpinnerAddFrame>`

