.. _MUIGetParentBackgroundColor:

===========================
MUIGetParentBackgroundColor 
===========================

MUIGetParentBackgroundColor, hWin::ref:`MUIWND<MUIWND>`

Gets a parent window background color. This function is useful for certain controls to retrieve the parent's background color and then to set their own background color based on the same value.

**Parameters**

* [in] **hWin** - handle to the window to get the parent color for


**Return**

Returns ``COLORREF`` or ``-1`` if a null brush is set for the window

**Example**

::
   
   LOCAL BackColor:COLORREF
   
   Invoke MUIGetParentBackgroundColor, hWin
   .IF eax != -1
      mov BackColor, eax
      ; Set controls own background based on parent's color
	  Invoke MUISetExtProperty, hWin, @MyControlBackColor, BackColor
   .ELSE
      ; Set default color if we couldn't get parents background color
      Invoke MUISetExtProperty, hWin, @MyControlBackColor, MUI_RGBCOLOR(240,240,240)
   .ENDIF

**See Also**

:ref:MUIGetParentBackgroundBitmap`<MUIGetParentBackgroundBitmap>`, :ref:`MUI_RGBCOLOR<MUI_RGBCOLOR>`

