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
   :glob:
   
   MUISmartPanel*


-----------------------------
ModernUI_SmartPanel Messages
-----------------------------



-------------------------------
ModernUI_SmartPanel Properties
-------------------------------
