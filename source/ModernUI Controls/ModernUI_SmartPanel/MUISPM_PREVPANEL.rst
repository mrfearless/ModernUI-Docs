.. _MUISPM_PREVPANEL:

===================================
MUISPM_PREVPANEL 
===================================

``MUISPM_PREVPANEL EQU WM_USER+1756``

A custom windows message for the ModernUI_SmartPanel control that moves to previous panel that is registered and shows it

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

None

**Example**

::

   Invoke SendMessage, hSmartPanel, MUISPM_PREVPANEL, NULL, NULL

**See Also**

:ref:`MUISmartPanelPrevPanel<MUISmartPanelPrevPanel>`, :ref:`MUISPM_NEXTPANEL<MUISPM_NEXTPANEL>`, :ref:`MUISmartPanelNextPanel<MUISmartPanelNextPanel>` 

