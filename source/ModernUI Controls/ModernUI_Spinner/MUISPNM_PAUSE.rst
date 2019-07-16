.. _MUISPNM_PAUSE:

===================================
MUISPNM_PAUSE 
===================================

``MUISPNM_PAUSE EQU WM_USER+1747``

A custom windows message for the ModernUI_Spinner that pauses the spinner animation

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_PAUSE, NULL, NULL

**See Also**

:ref:`MUISPNM_RESUME<MUISPNM_RESUME>`, :ref:`MUISPNM_ENABLE<MUISPNM_ENABLE>`, :ref:`MUISPNM_DISABLE<MUISPNM_DISABLE>`

