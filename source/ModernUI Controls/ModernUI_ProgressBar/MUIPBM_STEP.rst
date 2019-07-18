.. _MUIPBM_STEP:

===================================
MUIPBM_STEP 
===================================

``MUIPBM_STEP EQU WM_USER + 1750``

A custom windows message for the control that incrementally moves the progressbar

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hProgressBar, MUIPBM_STEP, NULL, NULL

**See Also**

:ref:`MUIPBM_SETPERCENT<MUIPBM_SETPERCENT>`

