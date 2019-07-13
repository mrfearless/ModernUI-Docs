.. _MUITextCreate:

========================
MUITextCreate 
========================

MUITextCreate, hWndParent::ref:`MUIWND<MUIWND>`, lpszText:LPSTR, X::ref:`MUIVALUE<MUIVALUE>`, Y::ref:`MUIVALUE<MUIVALUE>`, nWidth::ref:`MUIVALUE<MUIVALUE>`, nHeight::ref:`MUIVALUE<MUIVALUE>`, ResourceID::ref:`RESID<RESID>`, Style::ref:`MUIVALUE<MUIVALUE>`

Creates a new ModernUI_Text control.

**Parameters**

* [in] **hWndParent** - parent window of control
* [in] **lpszText** - text to display
* [in] **X** - x coord of control
* [in] **Y** - y coord of control
* [in] **nWidth** - width of control
* [in] **nHeight** - height of control
* [in] **ResourceID** - resource id of control
* [in] **Style** - can be combination of style flags, see :ref:`ModernUI_Text Style Flags<ModernUI_Text Style Flags>` for details

**Return**

Returns handle to newly created ModernUI_Text control (``MUIWND``) if successful, or ``NULL`` otherwise

.. _ModernUI_Text Style Flags:

**ModernUI_Text Style Flags**

The following combination of flags can be specified for **Style:**

*Font size style flags (a single flag from this group):*

* ``MUITS_7PT`` - 7pt
* ``MUITS_8PT`` - 8pt
* ``MUITS_9PT`` - 9pt
* ``MUITS_10PT`` - 10pt
* ``MUITS_11PT`` - 11pt
* ``MUITS_12PT`` - 12pt
* ``MUITS_13PT`` - 13pt
* ``MUITS_14PT`` - 14pt
* ``MUITS_15PT`` - 15pt
* ``MUITS_16PT`` - 16pt
* ``MUITS_18PT`` - 18pt
* ``MUITS_20PT`` - 20pt
* ``MUITS_22PT`` - 22pt
* ``MUITS_24PT`` - 24pt
* ``MUITS_28PT`` - 28pt
* ``MUITS_32PT`` - 32pt

*Font familty style flags (a single flag from this group):*

* ``MUITS_FONT_DIALOG`` - Use font that dialog is using
* ``MUITS_FONT_SEGOE`` - Segoe UI font
* ``MUITS_FONT_TAHOMA`` - Tahoma font
* ``MUITS_FONT_ARIAL`` - Arial font
* ``MUITS_FONT_TIMES`` - Times New Roman font
* ``MUITS_FONT_COURIER`` - Courier New font
* ``MUITS_FONT_VERDANA`` - Verdana font

*Text alignment style flags (a single flag from this group):*

* ``MUITS_ALIGN_LEFT`` - left align text
* ``MUITS_ALIGN_RIGHT`` - right align text
* ``MUITS_ALIGN_CENTER`` - center text
* ``MUITS_ALIGN_JUSTIFY`` - justify text

*Font special style flags (combination of flags allowed):*

* ``MUITS_FONT_NORMAL`` - No bold, italic or underline
* ``MUITS_FONT_BOLD`` - Bold text
* ``MUITS_FONT_ITALIC`` - Italic text
* ``MUITS_FONT_UNDERLINE`` - Underline text

*Misc options style flags (combination of flags allowed):*

* ``MUITS_SINGLELINE`` - Single line of text, otherwise is multi line
* ``MUITS_HAND`` - Show a hand instead of an arrow when mouse moves over text
* ``MUITS_LORUMIPSUM`` - Show lorum ipsum in text box - for demo purposes etc
* ``MUITS_UTF8`` - Text is utf8 format
* ``MUITS_HTMLCODE`` - Text has htmlcode tags to decode
* ``MUITS_BBCODE`` - Text has bbcode tags to decode


**Example**

::
   
   LOCAL TextStyle:DWORD
   
   mov TextStyle, MUITS_22PT or MUITS_FONT_SEGOE or MUITS_ALIGN_LEFT or MUITS_FONT_BOLD
   Invoke MUITextCreate, hWin, Addr szText, 10, 10, 400, 400, IDC_TXT1, TextStyle

**See Also**

:ref:`MUITextRegister<MUITextRegister>`, :ref:`MUITextSetProperty<MUITextSetProperty>`, :ref:`MUITextGetProperty<MUITextGetProperty>`

