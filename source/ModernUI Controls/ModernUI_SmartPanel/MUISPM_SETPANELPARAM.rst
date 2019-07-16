.. _MUISPM_SETPANELPARAM:

===================================
MUISPM_SETPANELPARAM 
===================================

``MUISPM_SETPANELPARAM EQU WM_USER+1752``

A custom windows message for the ModernUI_SmartPanel control that sets the panel's lParam of a registered panel which is custom user data

**Parameters**

* **wParam** - panel id to set panel's lParam for
* **lParam** - value to set panel's lParam to


**Return**

Returns lParam value if successful, or ``NULL`` otherwise

**Example**

::

   Invoke SendMessage, hSmartPanel, MUISPM_SETPANELPARAM, 1, 1234

**See Also**

:ref:`MUISPM_GETPANELPARAM<MUISPM_GETPANELPARAM>`
