

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/remap_axes:

remap_axes: Reorder, add and drop axes.
=======================================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` any.

Reorder, add and drop axes.



This transform allows the order of the input axes to be shuffled and
returned as the output axes.

It is a list made up of integers or "constant markers".  Each item
in the list corresponds to an output axis.  For each item:

-  If an integer, it is the index of the input axis to send to the
   output axis.

-  If a constant, it must be a single item which is a constant value
   to send to the output axis.

If only a list is provided, the number of input axes is
automatically determined from the maximum index in the list.  If an
object with :code:`mapping` and :code:`n_inputs` properties is provided, the
number of input axes is explicitly set by the :code:`n_inputs` value.

Invertibility: TBD



:category:`Definitions:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/remap_axes/definitions/mapping:

  :entry:`mapping`

  :soft:`Type:` array :soft:`of` ( integer :soft:`or` :doc:`constant <../core/constant>` ).

  

  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/remap_axes/definitions/mapping/items:

    :soft:`Type:` integer :soft:`or` :doc:`constant <../core/constant>`.

    

    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/0.1.0/transform/remap_axes/definitions/mapping/items/anyOf/0:

      :entry:`—`

      :soft:`Type:` integer.

      

      



      .. _http://stsci.edu/schemas/asdf/0.1.0/transform/remap_axes/definitions/mapping/items/anyOf/1:

      :entry:`—`

      :soft:`Type:` :doc:`constant <../core/constant>`.

      

      

:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/remap_axes/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/remap_axes/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

For 2 input axes, swap the axes::

  !transform/remap_axes
    mapping: [1, 0]
  

For 2 input axes, return the second axis and drop the first::

  !transform/remap_axes
    mapping: [1]
  

For 2 input axes, return the first axis twice, followed by the second::

  !transform/remap_axes
    mapping: [0, 0, 1]
  

For 2 input axes, add a third axis which is a constant::

  !transform/remap_axes
    mapping: [0, 1, !core/constant 42]
  

The above example is equivalent to the following, and ASDF
implementations are free to normalize it thusly:
::

  !transform/concatenate
    forward:
      - !transform/remap_axes
        mapping: [0]
      - !transform/remap_axes
        mapping: [1]
      - !transform/constant
        value: 42
  

Here we have 3 input axes, but we are explicitly dropping the last one::

  !transform/remap_axes
    mapping: [0, 1]
    n_inputs: 3
  

.. only:: html

   :download:`Original schema in YAML <remap_axes.yaml>`
