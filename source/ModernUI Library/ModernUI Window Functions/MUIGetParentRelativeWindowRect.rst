.. _MUIGetParentRelativeWindowRect:

==============================
MUIGetParentRelativeWindowRect 
==============================

MUIGetParentRelativeWindowRect, hWin::ref:`MUIWND<MUIWND>`, lpRectControl::ref:`LPRECT<LPRECT>`

Get rectangle of a window/control relative to it's parent.

**Parameters**

* [in] **hWin** - handle to the window to map the ``RECT`` (relative to it's parent) passed as the **lpRectControl** variable
* [in|out] **lpRectControl** - pointer to a ``RECT`` variable used to pass and store the rectangle to be adjusted relative to the parent of **hWin**


**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise. **lpRectControl** on successful return will contain the newly mapped rectangle coordinates.

**Example**

::

   LOCAL rect:RECT
   
   Invoke GetClientRect, hWin, Addr rect
   Invoke MUIGetParentRelativeWindowRect, hWin, Addr rect

**See Also**

:ref:`MUICenterWindow<MUICenterWindow>`

