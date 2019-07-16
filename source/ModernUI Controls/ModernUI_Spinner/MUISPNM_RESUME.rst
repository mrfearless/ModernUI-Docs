.. _MUISPNM_RESUME:

===================================
MUISPNM_RESUME 
===================================

``MUISPNM_RESUME EQU WM_USER+1746``

A custom windows message for the ModernUI_Spinner that resumes the spinner animation

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_RESUME, NULL, NULL

**See Also**

:ref:`MUISPNM_PAUSE<MUISPNM_PAUSE>`, :ref:`MUISPNM_ENABLE<MUISPNM_ENABLE>`, :ref:`MUISPNM_DISABLE<MUISPNM_DISABLE>`

