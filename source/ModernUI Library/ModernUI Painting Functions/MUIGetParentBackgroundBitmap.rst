.. _MUIGetParentBackgroundBitmap:

============================
MUIGetParentBackgroundBitmap 
============================

**MUIGetParentBackgroundBitmap, hControl:HWND**

Gets parent's background bitmap from the parent dc, at the child's location and size. For use in setting background of child to 'transparent'.


**Parameters**

* [in] **hControl** - handle to the window to get the parent bitmap for

**Return**

Returns a ``HBTIMAP`` if successful or ``NULL`` otherwise

**Example**

::
   
   LOCAL hBackBitmap:HBITMAP
   
   Invoke MUIGetParentBackgroundBitmap, hWin
   .IF eax != NULL
      mov hBackBitmap, eax
	  ; Store bitmap and use to paint our control's background to fake transparency
   .ENDIF

**See Also**

:ref:`MUIGetParentBackgroundColor<MUIGetParentBackgroundColor>`

