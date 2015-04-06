

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/add:

add: Perform a list of subtransforms in parallel and then add their results together.
=====================================================================================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` any.

Perform a list of subtransforms in parallel and then add their results together.



Each of the subtransforms must have the same number of inputs and
outputs.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/add/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/add/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

A list of transforms, performed in parallel and added together::

  !transform/add
    forward:
      - !transform/generic
        n_inputs: 1
        n_outputs: 2
      - !transform/generic
        n_inputs: 1
        n_outputs: 2
  

.. only:: html

   :download:`Original schema in YAML <add.yaml>`
