.. _MUISPNM_SPEED:

===================================
MUISPNM_SPEED
===================================

``MUISPNM_SPEED EQU WM_USER+1745``

A custom windows message for the ModernUI_Spinner that sets the spinner animation speed (in milliseconds)

**Parameters**

* **wParam** - speed in milliseconds for spinner animation
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSpinner, MUISPNM_SPEED, 100, NULL

**See Also**

:ref:`MUISPNM_PAUSE<MUISPNM_PAUSE>`, :ref:`MUISPNM_RESUME<MUISPNM_RESUME>`, :ref:`MUISPNM_ENABLE<MUISPNM_ENABLE>`, :ref:`MUISPNM_DISABLE<MUISPNM_DISABLE>`

