.. _MUISmartPanelSetCurrentPanel:

============================
MUISmartPanelSetCurrentPanel 
============================

MUISmartPanelSetCurrentPanel, hWin::ref:`MUIWND<MUIWND>`, PanelIndex::ref:`MUIVALUE<MUIVALUE>`, bNotify:BOOL

Sets the active panel to show, as specified via the panel index parameter PanelIndex. If panels are set to slide (animate) with any of the styles ``MUISPS_SLIDEPANELS_SLOW``, ``MUISPS_SLIDEPANELS_NORMAL``, ``MUISPS_SLIDEPANELS``, ``MUISPS_SLIDEPANELS_FAST``, ``MUISPS_SLIDEPANELS_VFAST`` they will slide from left to right. **bNotify** is an optional parameter that if ``TRUE`` will send a `WM_NOTIFY <https://docs.microsoft.com/en-us/windows/win32/controls/wm-notify>`_ message to the parent of the ModernUI_SmartPanel control with a code of ``MUISPN_SELCHANGED`` using a ``NM_MUISMARTPANEL`` structure

**Parameters**

* [in] **hWin** - handle to the ModernUI_SmartPanel control
* [in] **PanelIndex** - integer value of the panel index to set as the current active panel
* [in] **bNotify** - post notification that current panel has changed

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUISmartPanelSetCurrentPanel, hSP, 0

**See Also**

:ref:`MUISmartPanelGetCurrentPanel<MUISmartPanelGetCurrentPanel>`, :ref:`MUISmartPanelCurrentPanelIndex<MUISmartPanelCurrentPanelIndex>` 

