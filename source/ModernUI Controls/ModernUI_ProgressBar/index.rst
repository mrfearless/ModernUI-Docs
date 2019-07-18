.. _ModernUI_ProgressBar:

====================
ModernUI_ProgressBar
====================

.. image:: ModernUI_ProgressBar48x48.png

The ModernUI_ProgressBar is a progress bar control like the standard win32 progress bar control, except it provides ease of use and more customizable features, like color of the progress fill, the progress unfilled area and border.

------------------------------
ModernUI_ProgressBar Functions
------------------------------

.. toctree::
   :glob:
   :hidden:
   
   MUIProgressBar*

+-------------------------------------------------------------+-------------------------------------------------------------+
| **Function**                                                | **Description**                                             |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarCreate<MUIProgressBarCreate>`           | Creates a new ModernUI_ProgressBar control                  |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarGetPercent<MUIProgressBarGetPercent>`   | Gets the current percent value of the progressbar           |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarGetProperty<MUIProgressBarGetProperty>` | Gets the value of a property                                |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarRegister<MUIProgressBarRegister>`       | Registers a window class for the ModernUI_ProgressBar       |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarSetMinMax<MUIProgressBarSetMinMax>`     | Sets the minimum and maximum range of progressbar           |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarSetPercent<MUIProgressBarSetPercent>`   | Sets the current percent value of the progressbar           |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarSetProperty<MUIProgressBarSetProperty>` | Sets the value for a property                               |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIProgressBarStep<MUIProgressBarStep>`               | Incrementally moves the progressbar                         |
+-------------------------------------------------------------+-------------------------------------------------------------+


-----------------------------
ModernUI_ProgressBar Messages
-----------------------------

.. toctree::
   :hidden:
   :glob:
   
   MUIPBM*

+---------------------------------------------+-------------------------------------------------------------+
| **Message**                                 | **Description**                                             |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIPBM_SETPERCENT<MUIPBM_SETPERCENT>` | Sets the percentage of the progressbar                      |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUIPBM_STEP<MUIPBM_STEP>`             | Incrementally moves the progressbar one step                |
+---------------------------------------------+-------------------------------------------------------------+


.. _ModernUI_ProgressBar Properties:

-------------------------------
ModernUI_ProgressBar Properties
-------------------------------

+--------------------------------------------------------------------+--------------------------+
| **Property**                                                       | **Type**                 |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarTextColor<ProgressBarTextColorProperty>`         | ``MUICOLORRGB``          |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarTextFont<ProgressBarTextFontProperty>`           | ``HFONT``                |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarBackColor<ProgressBarBackColorProperty>`         | ``MUICOLORRGB``          |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarProgressColor<ProgressBarProgressColorProperty>` | ``MUICOLORRGB``          |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarBorderColor<ProgressBarBorderColorProperty>`     | ``MUICOLORRGB``          |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarPercent<ProgressBarPercentProperty>`             | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarMin<ProgressBarMinProperty>`                     | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarMax<ProgressBarMaxProperty>`                     | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarStep<ProgressBarStepProperty>`                   | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarPulse<ProgressBarPulseProperty>`                 | ``BOOL``                 |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarPulseTime<ProgressBarPulseTimeProperty>`         | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarTextType<ProgressBarTextTypeProperty>`           | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@ProgressBarSetTextPos<ProgressBarSetTextPosProperty>`       | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+


ModernUI_ProgressBar Property Descriptions
------------------------------------------


.. _ProgressBarTextColorProperty:

**ProgressBarTextColor**

Color of percentage text (:ref:`MUICOLORRGB<MUICOLORRGB>`) of the ModernUI_ProgressBar control.

.. _ProgressBarTextFontProperty:

**ProgressBarTextFont**

Font (HFONT) used for the progress bar text

.. _ProgressBarBackColorProperty:

**ProgressBarBackColor**

Background color (:ref:`MUICOLORRGB<MUICOLORRGB>`) of the ModernUI_ProgressBar control.

.. _ProgressBarProgressColorProperty:

**ProgressBarProgressColor**

Progress bar percent filled color (:ref:`MUICOLORRGB<MUICOLORRGB>`) of the ModernUI_ProgressBar control.

.. _ProgressBarBorderColorProperty:

**ProgressBarBorderColor**

Border color (:ref:`MUICOLORRGB<MUICOLORRGB>`) of the ModernUI_ProgressBar control.

.. _ProgressBarPercentProperty:

**ProgressBarPercent**

Current progress bar percentage value

.. _ProgressBarMinProperty:

**ProgressBarMin**

Minimum range value - `currently not implemented`

.. _ProgressBarMaxProperty:

**ProgressBarMax**

Maximum range value - `currently not implemented`

.. _ProgressBarStepProperty:

**ProgressBarStep**

Value to increment the progress bar when calling :ref:`MUIProgressBarStep<MUIProgressBarStep>` or :ref:`MUIPBM_STEP<MUIPBM_STEP>`. Defaults to ``1`` - `currently not implemented`

.. _ProgressBarPulseProperty:

**ProgressBarPulse**

Enable pulse glow effect to show progress bar is still active. ``TRUE`` to enable, ``FALSE`` to disable. Default is ``TRUE``

.. _ProgressBarPulseTimeProperty:

**ProgressBarPulseTime**

Time in milliseconds between pulse effect is shown. Defaults to 5 seconds (5000ms)

.. _ProgressBarTextTypeProperty:

**ProgressBarTextType**

Type of percentage text to display, can be one of the following values:

- ``MUIPBTT_NONE``- no percentage text in progress bar (default)
- ``MUIPBTT_CENTRE`` - percentage text in center of progress bar
- ``MUIPBTT_FOLLOW`` - percentage text follows progress as it draws

.. _ProgressBarSetTextPosProperty:

**ProgressBarSetTextPos**

Position of other text, can be one of the following values: ``0`` = preppend WM_SETTEXT text, ``1`` = append WM_SETTEXT text `currently not implemented`




