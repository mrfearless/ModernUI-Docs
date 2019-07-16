.. _MUISPM_NEXTPANEL:

===================================
MUISPM_NEXTPANEL 
===================================

``MUISPM_NEXTPANEL EQU WM_USER+1757``

A custom windows message for the ModernUI_SmartPanel control that moves to next panel that is registered and shows it

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSmartPanel, MUISPM_NEXTPANEL, NULL, NULL

**See Also**

:ref:`MUISmartPanelNextPanel<MUISmartPanelNextPanel>`, :ref:`MUISPM_PREVPANEL<MUISPM_PREVPANEL>`, :ref:`MUISmartPanelPrevPanel<MUISmartPanelPrevPanel>` 

