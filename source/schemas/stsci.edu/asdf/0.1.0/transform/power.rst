

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/power:

power: Perform a list of subtransforms in parallel and then raise each result to the power of the next.
=======================================================================================================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` any.

Perform a list of subtransforms in parallel and then raise each result to the power of the next.



Each of the subtransforms must have the same number of inputs and
outputs.

Invertibility: This transform is not automatically invertible.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/power/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/power/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

.. only:: html

   :download:`Original schema in YAML <power.yaml>`
