.. _ModernUI_SmartPanel:

====================
ModernUI_SmartPanel
====================

.. image:: ModernUI_SmartPanel48x48.png

The ModernUI_SmartPanel is an invisible control - it is only shown during design time (if using the RadASM design-time dll for the ModernUI_SmartPanel). Its purpose is to host other dialog panels, and facilitate moving between dialog panels seemlessly. It can also provide a slide effect when changing from one panel to another.

The ModernUI_SmartPanel control can also control the painting of the background for the dialog panels that are registered with it. Additionally it will adjust each panel's style at registration so that it is flat, borderless and without a caption, and set the DS_CONTROL flag for its style. If using IsDIalogMessage in your message loop, the ModernUI_SmartPanel control can store the handle of the currently used dialog panel, in a variable that can be used with the IsDialogMessage during the event loop, so that you can provide tabbing between controls of the hosted dialog panel's controls.

------------------------------
ModernUI_SmartPanel Functions
------------------------------

.. toctree::
   :hidden:
   :glob:
   
   MUISmartPanel*


+-----------------------------------------------------------------------+-------------------------------------------------------------+
| **Function**                                                          | **Description**                                             |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelCreate<MUISmartPanelCreate>`                       | Creates a new ModernUI_SmartPanel control                   |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelCurrentPanelIndex<MUISmartPanelCurrentPanelIndex>` | Gets the current panel's index                              |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelGetCurrentPanel<MUISmartPanelGetCurrentPanel>`     | Gets handle (``HWND``) to current active panel              |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelGetPanelParam<MUISmartPanelGetPanelParam>`         | Get lParam of panel - custom user data                      |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelGetProperty<MUISmartPanelGetProperty>`             | Gets the value of a property                                |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelNextPanel<MUISmartPanelNextPanel>`                 | Moves to next panel that is registered and shows it         |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelNotifyCallback<MUISmartPanelNotifyCallback>`       | User specified callback for notifications                   |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelPrevPanel<MUISmartPanelPrevPanel>`                 | Moves to previous panel that is registered and shows it     |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelRegister<MUISmartPanelRegister>`                   | Registers a window class for the ModernUI_SmartPanel        |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelRegisterPanel<MUISmartPanelRegisterPanel>`         | Registers a dialog window (``HWND``) with the SmartPanel    |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelSetCurrentPanel<MUISmartPanelSetCurrentPanel>`     | Sets the current active panel                               |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelSetIsDlgMsgVar<MUISmartPanelSetIsDlgMsgVar>`       | Variable to receive current panel handle                    |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelSetPanelParam<MUISmartPanelSetPanelParam>`         | Sets the lParam of a registered panel - custom user data    |
+-----------------------------------------------------------------------+-------------------------------------------------------------+
| :ref:`MUISmartPanelSetProperty<MUISmartPanelSetProperty>`             | Sets the value of a property                                |
+-----------------------------------------------------------------------+-------------------------------------------------------------+





-----------------------------
ModernUI_SmartPanel Messages
-----------------------------

+---------------------------+-------------------------------------------------------------+
| **Message**               | **Description**                                             |
+---------------------------+-------------------------------------------------------------+
| MUISPM_REGISTERPANEL      | Registers a dialog window (``HWND``) with the SmartPanel    |
+---------------------------+-------------------------------------------------------------+
| MUISPM_SETCURRENTPANEL    | Sets the current active panel                               |
+---------------------------+-------------------------------------------------------------+
| MUISPM_GETCURRENTPANEL    | Gets the current panel's index                              |
+---------------------------+-------------------------------------------------------------+
| MUISPM_NEXTPANEL          | Moves to next panel that is registered and shows it         |
+---------------------------+-------------------------------------------------------------+
| MUISPM_PREVPANEL          | Moves to previous panel that is registered and shows it     |
+---------------------------+-------------------------------------------------------------+
| MUISPM_GETTOTALPANELS     | Gets total panels registered with the SmartPanel control    |
+---------------------------+-------------------------------------------------------------+
| MUISPM_SETISDLGMSGVAR     | Variable to receive current panel handle                    |
+---------------------------+-------------------------------------------------------------+
| MUISPM_GETPANELPARAM      | Get lParam of panel - custom user data                      |
+---------------------------+-------------------------------------------------------------+
| MUISPM_SETPANELPARAM      | Sets the lParam of a registered panel - custom user data    |
+---------------------------+-------------------------------------------------------------+


.. _ModernUI_SmartPanel Properties:

-------------------------------
ModernUI_SmartPanel Properties
-------------------------------

+--------------------------------------------------------------------+--------------------------+
| **Property**                                                       | **Type**                 |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@SmartPanelPanelsColor<SmartPanelPanelsColorProperty>`       | ``MUICOLORRGB``          |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@SmartPanelBorderColor<SmartPanelBorderColorProperty>`       | ``MUICOLORRGB``          |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@SmartPanelNotifications<SmartPanelNotificationsProperty>`   | ``BOOL``                 |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@SmartPanelNotifyCallback<SmartPanelNotifyCallbackProperty>` | ``POINTER``              |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@SmartPanelDllInstance<SmartPanelDllInstanceProperty>`       | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+
| :ref:`@SmartPanelParam<SmartPanelParamProperty>`                   | ``MUIVALUE``             |
+--------------------------------------------------------------------+--------------------------+


ModernUI_SmartPanel Property Descriptions
-----------------------------------------

.. _SmartPanelPanelsColorProperty:

**@SmartPanelPanelsColor**

Back color (:ref:`MUICOLORRGB<MUICOLORRGB>`) for registered panels. If set to ``-1`` then uses system default. Default is ``-1``

.. _SmartPanelBorderColorProperty:

**@SmartPanelBorderColor**

Border color (:ref:`MUICOLORRGB<MUICOLORRGB>`) for registered panels. If set to ``-1`` then no border. Default value is ``-1``

.. _SmartPanelNotificationsProperty:

**@SmartPanelNotifications**

Enable or disable notifications via `WM_NOTIFY <https://docs.microsoft.com/en-us/windows/win32/controls/wm-notify>`_ or **@SmartPanelNotifyCallback**. Default is ``TRUE``

.. _SmartPanelNotifyCallbackProperty:

**@SmartPanelNotifyCallback**

Address of custom notification callback to use instead of `WM_NOTIFY <https://docs.microsoft.com/en-us/windows/win32/controls/wm-notify>`_. If set to ``NULL`` uses `WM_NOTIFY <https://docs.microsoft.com/en-us/windows/win32/controls/wm-notify>`_. Default is ``NULL``

.. _SmartPanelDllInstanceProperty:

**@SmartPanelDllInstance**

Instance value for use in dll. Future use.

.. _SmartPanelParamProperty:

**@SmartPanelParam**

Custom user defined value to assign to ModernUI_SmartPanel control.

