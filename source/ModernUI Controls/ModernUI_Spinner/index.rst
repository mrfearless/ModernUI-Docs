.. _ModernUI_Spinner:

====================
ModernUI_Spinner
====================

.. image:: ModernUI_Spinner48x48.png

The ModernUI_Spinner is a control typically used when loading, pre-loading or processing something and to hint or indicate to the user something is occurring.

------------------------------
ModernUI_Spinner Functions
------------------------------

.. toctree::
   :hidden:
   :glob:
   
   MUISpinner*

+-------------------------------------------------------------+-------------------------------------------------------------+
| **Function**                                                | **Description**                                             |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerAddFrame<MUISpinnerAddFrame>`               | Adds an image handle (previously loaded) to the control     |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerAddFrames<MUISpinnerAddFrames>`             | Adds an array of image handles (previously loaded)          |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerAddImage<MUISpinnerAddImage>`               | Adds a single image handle (previously loaded), to rotate   |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerAddSpriteSheet<MUISpinnerAddSpriteSheet>`   | Adds a spritesheet - an imagestrip of animation frames      |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerCreate<MUISpinnerCreate>`                   | Creates a new ModernUI_Spinner control                      |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerDisable<MUISpinnerDisable>`                 | Disable and hide the spinner animation                      |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerEnable<MUISpinnerEnable>`                   | Enable and show the spinner animation                       |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerGetProperty<MUISpinnerGetProperty>`         | Gets the value of a property                                |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerLoadFrame<MUISpinnerLoadFrame>`             | Loads an image from a resource and adds to the control      |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerLoadFrames<MUISpinnerLoadFrames>`           | Loads an array of resources and adds the frames             |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerLoadImage<MUISpinnerLoadImage>`             | Loads a single image from a resource, to rotate             |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerLoadSpriteSheet<MUISpinnerLoadSpriteSheet>` | Loads a spritesheet from a resource                         |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerPause<MUISpinnerPause>`                     | Pause the spinner animation                                 |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerRegister<MUISpinnerRegister>`               | Registers a window class for the ModernUI_Spinner           |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerReset<MUISpinnerReset>`                     | Reset the spinner's current frame                           |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerResume<MUISpinnerResume>`                   | Resume the spinner animation                                |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerSetProperty<MUISpinnerSetProperty>`         | Sets the value for a property                               |
+-------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISpinnerSpeed<MUISpinnerSpeed>`                     | Set the spinner animation speed (in milliseconds)           |
+-------------------------------------------------------------+-------------------------------------------------------------+



-----------------------------
ModernUI_Spinner Messages
-----------------------------

.. toctree::
   :hidden:
   :glob:
   
   MUISPNM*

+---------------------------------------------+-------------------------------------------------------------+
| **Message**                                 | **Description**                                             |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_ADDFRAME<MUISPNM_ADDFRAME>`   | Adds an image handle (previously loaded) to the control     |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_DISABLE<MUISPNM_DISABLE>`     | Disable and hide the spinner animation                      |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_ENABLE<MUISPNM_ENABLE>`       | Enable and show the spinner animation                       |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_LOADFRAME<MUISPNM_LOADFRAME>` | Loads an image from a resource and adds to the control      |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_PAUSE<MUISPNM_PAUSE>`         | Pause the spinner animation                                 |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_RESET<MUISPNM_RESET>`         | Reset the spinner's current frame                           |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_RESUME<MUISPNM_RESUME>`       | Resume the spinner animation                                |
+---------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISPNM_SPEED<MUISPNM_SPEED>`         | Set the spinner animation speed (in milliseconds)           |
+---------------------------------------------+-------------------------------------------------------------+


-----------------------------
ModernUI_Spinner Properties
-----------------------------

+------------------------------------------------------------------+--------------------------+
| **Property**                                                     | **Type**                 |
+------------------------------------------------------------------+--------------------------+
| :ref:`@SpinnerBackColor<SpinnerBackColorProperty>`               | ``MUICOLORRGB``          |
+------------------------------------------------------------------+--------------------------+
| :ref:`@SpinnerSpeed<SpinnerSpeedProperty>`                       | ``MUIVALUE``             |
+------------------------------------------------------------------+--------------------------+
| :ref:`@SpinnerDllInstance<SpinnerDllInstanceProperty>`           | ``HINSTANCE``            |
+------------------------------------------------------------------+--------------------------+



ModernUI_Spinner Property Descriptions
--------------------------------------

.. _SpinnerBackColorProperty:

**@SpinnerBackColor**

Background color (:ref:`MUICOLORRGB<MUICOLORRGB>`) of the ModernUI_Spinner control. By default will try to obtain the color of the parent's background color otherwise will default to GetSysColor value returned by ``COLOR_WINDOW``

.. _SpinnerSpeedProperty:

**@SpinnerSpeed**
   
A value (:ref:`MUIVALUE<MUIVALUE>`) indicating speed in milliseconds of the ModernUI_Spinner control frame animation. Default speed is ``80`` milliseconds

.. _SpinnerDllInstanceProperty:

**@SpinnerDllInstance**

Used for loading resources when ModernUI_Spinner control is used in a dll. Default is ``NULL``


