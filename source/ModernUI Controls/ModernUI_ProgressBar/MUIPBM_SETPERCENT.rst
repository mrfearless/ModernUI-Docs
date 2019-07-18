.. _MUIPBM_SETPERCENT:

===================================
MUIPBM_SETPERCENT 
===================================

``MUIPBM_SETPERCENT EQU WM_USER + 1749``

A custom windows message for the control that sets the current percent value of the progressbar

**Parameters**

* **wParam** - value to set percentage of the progress bar to
* **lParam** - ``NULL``

**Return**

None

**Example**

::

   Invoke SendMessage, hProgressBar, MUIPBM_SETPERCENT, 50, NULL

**See Also**

:ref:`MUIPBM_STEP<MUIPBM_STEP>`

