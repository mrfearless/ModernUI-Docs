.. _MUIApplyToDialog:

========================
MUIApplyToDialog 
========================

MUIApplyToDialog, hWin::ref:`MUIWND<MUIWND>`, bDropShadow:BOOL, bClipping:BOOL

Applies the ModernUI style to a dialog to make it a captionless, borderless form. User can manually change a form in a resource editor to have the following style flags: ``WS_POPUP`` or ``WS_VISIBLE`` and optionally with ``DS_CENTER``, ``DS_CENTERMOUSE``, ``WS_CLIPCHILDREN``, ``WS_CLIPSIBLINGS``, ``WS_MINIMIZE``, ``WS_MAXIMIZE``

**Parameters**

* [in] **hWin** - handle to window to apply the ModernUI look
* [in] **bDropShadow** - show drop shadow on dialog/window ``TRUE`` or ``FALSE``
* [in] **bClipping** - enable clipping on dialog/window ``TRUE`` or ``FALSE``


**Return**

None

**Example**

::

   Invoke MUIApplyToDialog, TRUE, FALSE


