.. _MUILoadRegionFromResource:

=========================
MUILoadRegionFromResource 
=========================

MUILoadRegionFromResource, hInst:HINSTANCE, idRgnRes::ref:`RESID<RESID>`, lpRegionData::ref:`POINTER<POINTER>`, lpSizeRegionData::ref:`LPMUIVALUE<LPMUIVALUE>` 

Loads region data from a resource, stored as ``RC_DATA``.


**Parameters**

* [in] **hInst** - instance of the exe/dll to use for loading resources
* [in] **idRgnRes** - resource id of the region ``RC_DATA`` resource to load
* [out] **lpRegionData** - pointer to a variable to store the loaded region
* [out] **lpSizeRegion** - pointer to a variable to store the size of the region data


**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   LOCAL hinstance:DWORD
   LOCAL ptrRegionData:DWORD
   LOCAL dwRegionDataSize:DWORD
   LOCAL hRgn:DWORD
   
   Invoke GetModuleHandle, NULL
   mov hinstance, eax
   
   ; Load region data from resource
   Invoke MUILoadRegionFromResource, hinstance, idRgnRes, Addr ptrRegionData, Addr dwRegionDataSize
   
   ; clear existing region if any from window
   Invoke SetWindowRgn, hWin, NULL, FALSE
   
   ; create region based on our loaded region data
   Invoke ExtCreateRegion, NULL, dwRegionDataSize, ptrRegionData
   mov hRgn, eax
   .IF eax == NULL
      ; error couldnt create region so exit
      ret
   .ENDIF
   
   ; Set window to our newly created region (from our loaded region data)
   Invoke SetWindowRgn, hWin, hRgn, TRUE
	

**See Also**

:ref:`MUISetRegionFromResource<MUISetRegionFromResource>`

