.. only:: html

   |updatedisclaimer|

.. _`processing.options`:

**************************************
 Configuring the Processing Framework
**************************************

.. only:: html

   .. contents::
      :local:
      

As has been mentioned, the configuration menu gives access to a new dialog
where you can configure how algorithms work. Configuration parameters are
structured in separate blocks that you can select on the left-hand side of the
dialog.

Along with the aforementioned :guilabel:`Output folder` entry, the
:guilabel:`General` block contains parameters for setting the default rendering
style for output layers (that is, layers generated by using algorithms from
any of the framework GUI components). Just create the style you want using QGIS, save
it to a file, and then enter the path to that file in the settings so the algorithms
can use it. Whenever a layer is loaded by Processing and added to the
QGIS canvas, it will be rendered with that style.

Rendering styles can be configured individually for each algorithm and each one
of its outputs. Just right-click on the name of the algorithm in the toolbox and
select :guilabel:`Edit rendering styles for outputs`. You will see a dialog like
the one shown next.

.. _figure_rendering_styles:

.. figure:: img/rendering_styles.png
   :align: center

   Rendering Styles

Select the style file (:file:`.qml`) that you want for each output and press
:guilabel:`OK`.

Other configuration parameters in the :guilabel:`General` group are listed below:

* :guilabel:`Use filename as layer name`. The name of each resulting layer created
  by an algorithm is defined by the algorithm itself. In some cases, a fixed
  name might be used, meaning that the same output name will be used, no matter
  which input layer is used. In other cases, the name might depend on the name
  of the input layer or some of the parameters used to run the algorithm. If this
  checkbox is checked, the name will be taken from the output filename instead.
  Notice that, if the output is saved to a temporary file, the filename of this
  temporary file is usually a long and meaningless one intended to avoid collision
  with other already existing filenames.
* :guilabel:`Keep dialog open after running algorithm`. Once an algorithm has
  finished execution and its output layers are loaded into the QGIS project,
  the algorithm dialog is closed. If you want to keep it open (to run the algorithm
  again with different parameters, or to better check the output that is written
  to the log tab), check this option
* :guilabel:`Use only selected features`. If this option is selected, whenever a
  vector layer is used as input for an algorithm, only its selected features will
  be used. If the layer has no selected features, all features will be used.
* :guilabel:`Pre-execution script file` and :guilabel:`Post-execution script file`.
  These parameters refer to scripts written using the processing scripting
  functionality, and are explained in the section covering scripting and the
  console.

Apart from the :guilabel:`General` block in the settings dialog, you will also
find a block for algorithm providers. Each entry in this block contains an :guilabel:`Activate` item
that you can use to make algorithms appear or not in the toolbox. Also, some
algorithm providers have their own configuration items, which we will explain later
when covering particular algorithm providers.


.. Substitutions definitions - AVOID EDITING PAST THIS LINE
   This will be automatically updated by the find_set_subst.py script.
   If you need to create a new substitution manually,
   please add it also to the substitutions.txt file in the
   source folder.

.. |updatedisclaimer| replace:: :disclaimer:`Docs in progress for 'QGIS testing'. Visit https://docs.qgis.org/2.18 for QGIS 2.18 docs and translations.`
