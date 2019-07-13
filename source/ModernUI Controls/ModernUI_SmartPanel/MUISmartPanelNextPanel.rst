.. _MUISmartPanelNextPanel:

========================
MUISmartPanelNextPanel 
========================

MUISmartPanelNextPanel, hWin::ref:`MUIWND<MUIWND>`, bNotify:BOOL

Sets the active current panel to the next panel. If style ``MUISPS_SPS_WRAPAROUND`` is specified at creation, the panel will move and wrap around from the last panel to the first panel if it is currently at the last panel, instead of doing nothing. If panels are set to slide (animate) with any of the styles ``MUISPS_SLIDEPANELS_SLOW``, ``MUISPS_SLIDEPANELS_NORMAL``, ``MUISPS_SLIDEPANELS``, ``MUISPS_SLIDEPANELS_FAST``, ``MUISPS_SLIDEPANELS_VFAST`` they will slide from left to right. **bNotify** is an optional parameter that if ``TRUE`` will send a `WM_NOTIFY <https://docs.microsoft.com/en-us/windows/win32/controls/wm-notify>`_ message to the parent of the ModernUI_SmartPanel control with a code of ``MUISPN_SELCHANGED`` using a ``NM_MUISMARTPANEL`` structure

**Parameters**

* [in] **hWin** - handle to the ModernUI_SmartPanel control
* [in] **bNotify** - post notification that current panel has changed

**Return**

None

**Example**

::

   Invoke MUISmartPanelNextPanel, hSP, TRUE

**See Also**

:ref:`MUISmartPanelPrevPanel<MUISmartPanelPrevPanel>`, :ref:`MUISmartPanelSetCurrentPanel<MUISmartPanelSetCurrentPanel>`, :ref:`ModernUI_SmartPanel Style Flags<ModernUI_SmartPanel Style Flags>`

