.. _MUISPM_GETCURRENTPANEL:

===================================
MUISPM_GETCURRENTPANEL 
===================================

``MUISPM_GETCURRENTPANEL EQU WM_USER+1758``

A custom windows message for the ModernUI_SmartPanel control that gets the current panel's index

**Parameters**

* **wParam** - ``NULL``
* **lParam** - ``NULL``


**Return**

Returns panel index

**Example**

::

   Invoke SendMessage, hSmartPanel, MUISPM_GETCURRENTPANEL, NULL, NULL

**See Also**

:ref:`MUISPM_SETCURRENTPANEL<MUISPM_SETCURRENTPANEL>`, :ref:`MUISmartPanelSetCurrentPanel<MUISmartPanelSetCurrentPanel>`, :ref:`MUISmartPanelGetCurrentPanel<MUISmartPanelGetCurrentPanel>`, :ref:`MUISmartPanelCurrentPanelIndex<MUISmartPanelCurrentPanelIndex>`

