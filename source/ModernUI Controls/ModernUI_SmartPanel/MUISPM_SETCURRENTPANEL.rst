.. _MUISPM_SETCURRENTPANEL:

===================================
MUISPM_SETCURRENTPANEL 
===================================

``MUISPM_SETCURRENTPANEL EQU WM_USER+1759``

A custom windows message for the ModernUI_SmartPanel control that sets the current active panel

**Parameters**

* **wParam** - panel id to select
* **lParam** - send notify message: ``TRUE`` or ``FALSE``


**Return**

Returns the index of the previously selected panel if successful or ``-1`` otherwise.

**Example**

::

   Invoke SendMessage, hSmartPanel, MUISPM_SETCURRENTPANEL, 1, TRUE

**See Also**

:ref:`MUISPM_GETCURRENTPANEL<MUISPM_GETCURRENTPANEL>`, :ref:`MUISmartPanelGetCurrentPanel<MUISmartPanelGetCurrentPanel>`, :ref:`MUISmartPanelSetCurrentPanel<MUISmartPanelSetCurrentPanel>`, :ref:`MUISmartPanelCurrentPanelIndex<MUISmartPanelCurrentPanelIndex>`

