.. _MUICenterWindow:

========================
MUICenterWindow 
========================

**MUICenterWindow, hWndChild:HWND, hWndParent:HWND**

Center a child window **hWndChild** into parent window **hWndParent** (or desktop if **hWndParent** is ``NULL``). Parent doesn't need to be the owner.


**Parameters**

* [in] **hWndChild** - handle to child window to center
* [in] **hWndParent** - parent window of child to center, relative to


**Return**

None

**Example**

::

   Invoke GetParent, hWin
   mov hParent, eax
   Invoke MUICenterWindow, hWin, hParent

**See Also**

:ref:`MUIGetParentRelativeWindowRect<MUIGetParentRelativeWindowRect>`

