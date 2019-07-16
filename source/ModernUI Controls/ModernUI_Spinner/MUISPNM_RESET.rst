.. _MUISPNM_RESET:

===================================
MUISPNM_RESET 
===================================

``MUISPNM_RESET EQU WM_USER+1748``

A custom windows message for the ModernUI_Spinner that reset the spinner's current frame

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_RESET, NULL, NULL

**See Also**

:ref:`MUISPNM_ENABLE<MUISPNM_ENABLE>`, :ref:`MUISPNM_DISABLE<MUISPNM_DISABLE>`

