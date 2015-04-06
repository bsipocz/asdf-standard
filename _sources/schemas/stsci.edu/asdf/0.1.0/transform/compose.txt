

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/compose:

compose: Perform a list of subtransforms in series.
===================================================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` any.

Perform a list of subtransforms in series.



The output of each subtransform is fed into the input of the next
subtransform.

The number of output dimensions of each subtransform must be equal
to the number of input dimensions of the next subtransform in list.
To reorder or add/drop axes, insert :code:`remap_axes` transforms in the
subtransform list.

Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform, by reversing the list of
transforms and applying the inverse of each.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/compose/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/compose/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

A series of transforms::

  !transform/compose
    forward:
      - !transform/generic
        n_inputs: 1
        n_outputs: 2
      - !transform/generic
        n_inputs: 2
        n_outputs: 1
  

.. only:: html

   :download:`Original schema in YAML <compose.yaml>`
