.. _MUISPM_GETPANELPARAM:

===================================
MUISPM_GETPANELPARAM 
===================================

``MUISPM_GETPANELPARAM EQU WM_USER+1753``

A custom windows message for the ModernUI_SmartPanel control that gets the lParam of a panel which is custom user data

**Parameters**

* **wParam** - panel id to get panel's lParam for
* **lParam** - ``NULL``


**Return**

Returns panel lParam value if successful, or ``NULL`` otherwise

**Example**

::

   Invoke SendMessage, hSmartPanel, MUISPM_GETPANELPARAM, 1, NULL

**See Also**

:ref:`MUISPM_SETPANELPARAM<MUISPM_SETPANELPARAM>`

