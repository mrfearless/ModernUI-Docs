.. _MUISPNM_ENABLE:

===================================
MUISPNM_ENABLE 
===================================

``MUISPNM_ENABLE EQU WM_USER+1750``

A custom windows message for the ModernUI_Spinner that enables and shows the spinner animation

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_ENABLE, NULL, NULL

**See Also**

:ref:`MUISPNM_DISABLE<MUISPNM_DISABLE>`, :ref:`MUISPNM_PAUSE<MUISPNM_PAUSE>`

