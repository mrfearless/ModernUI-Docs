.. _MUISPNM_DISABLE:

===================================
MUISPNM_DISABLE 
===================================

``MUISPNM_DISABLE EQU WM_USER+1749``

A custom windows message for the ModernUI_Spinner that disables and hides the spinner animation

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_DISABLE, NULL, NULL

**See Also**

:ref:`MUISPNM_ENABLE<MUISPNM_ENABLE>`, :ref:`MUISPNM_RESUME<MUISPNM_RESUME>`

