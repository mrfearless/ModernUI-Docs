.. _MUIProgressBarSetPercent:

========================
MUIProgressBarSetPercent 
========================

MUIProgressBarSetPercent, hWin::ref:`MUIWND<MUIWND>`, Percent::ref:`MUIVALUE<MUIVALUE>`

Sets the current percent value of the progressbar

**Parameters**

* [in] **hWin** - handle to the ModernUI_ProgressBar control
* [in] **Percent** - value to set percentage of the progress bar to

**Return**

Returns ``TRUE`` if successful, or ``FALSE`` otherwise

**Example**

::

   Invoke MUIProgressBarSetPercent, hProgressBar, 50

**See Also**

:ref:`MUIProgressBarGetPercent<MUIProgressBarGetPercent>`, :ref:`MUIProgressBarStep<MUIProgressBarStep>`

