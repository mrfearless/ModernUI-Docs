.. _MUISPM_GETTOTALPANELS:

===================================
MUISPM_GETTOTALPANELS 
===================================

``MUISPM_GETTOTALPANELS EQU WM_USER+1755``

A custom windows message for the ModernUI_SmartPanel control that returns total panels registered

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

Returns total panels registered, or ``-1`` if no panels registered

**Example**

::

   Invoke SendMessage, hSmartPanel, MUISPM_GETTOTALPANELS, NULL, NULL

**See Also**

:ref:`MUISPM_GETCURRENTPANEL<MUISPM_GETCURRENTPANEL>`, :ref:`MUISPM_SETCURRENTPANEL<MUISPM_SETCURRENTPANEL>`, :ref:`MUISmartPanelSetCurrentPanel<MUISmartPanelSetCurrentPanel>`, :ref:`MUISmartPanelGetCurrentPanel<MUISmartPanelGetCurrentPanel>`, :ref:`MUISmartPanelCurrentPanelIndex<MUISmartPanelCurrentPanelIndex>`

