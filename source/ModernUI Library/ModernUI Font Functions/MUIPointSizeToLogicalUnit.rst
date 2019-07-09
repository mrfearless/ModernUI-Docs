.. _MUIPointSizeToLogicalUnit:

=========================
MUIPointSizeToLogicalUnit 
=========================

**MUIPointSizeToLogicalUnit, hWin:HWND, PointSize:SIZE_T**

Convert font point size eg ``12`` to logical unit size for use with `CreateFont <https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-createfonta>`_ or `CreateFontIndirect <https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-createfontindirecta>`_

**Parameters**

* [in] **hWin** - handle to window to use dc for converting the point size to logical size
* [in] **PointSize** - a value representing the point size to convert


**Return**

Returns the font height for the point size specified

**Example**

::
   
   LOCAL dwFontHeight:DWORD
   
   MUIPointSizeToLogicalUnit, hWin, 12
   mov dwFontHeight, eax
   
   Invoke CreateFont, dwFontHeight, ...
   

**See Also**

`CreateFont <https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-createfonta>`_, `CreateFontIndirect <https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-createfontindirecta>`_

