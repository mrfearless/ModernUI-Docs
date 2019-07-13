.. _MUISetRegionFromResource:

========================
MUISetRegionFromResource 
========================

MUISetRegionFromResource, hWin::ref:`MUIWND<MUIWND>`, idRgnRes::ref:`RESID<RESID>`, lpCopyRgnHandle::ref:`LPMUIVALUE<LPMUIVALUE>`, bRedraw:BOOL

Sets a window/controls region from a region stored as an ``RC_DATA`` resource: **idRgnRes**. If **lpdwCopyRgn** is not ``NULL`` a copy of region handle is provided (for any future calls to `FrameRgn <https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-framergn>`_ for example). This function internally calls the :ref:`MUILoadRegionFromResource<MUILoadRegionFromResource>` function.

**Parameters**

* [in] **hWin** - handle to the window to set a region for
* [in] **idRgnRes** - resource id of the region ``RC_DATA`` resource to load
* [out] **lpCopyRgn** - pointer to a variable to store a copy of the loaded region
* [in] **bRedraw** - redraw the window after the region is set (``TRUE`` or ``FALSE``)

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   .const
   RGN_MAP_EUROPE EQU 300 ; resource stored as id 300 in RC_DATA format

::
   
   LOCAL hRegCopyMapEurope:DWORD

   Invoke MUISetRegionFromResource, hWin, RGN_MAP_EUROPE, Addr hRegCopyMapEurope, TRUE
   ; hWin should now be shaped like a map of europe

**See Also**

:ref:`MUILoadRegionFromResource<MUILoadRegionFromResource>`, `FrameRgn <https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-framergn>`_

