

.. _http://stsci.edu/schemas/asdf/0.1.0/wcs/wcs:

wcs: A system for describing generalized world coordinate transformations.
==========================================================================

:soft:`Type:` object.

A system for describing generalized world coordinate transformations.



ASDF WCS is a way of specifying transformations (usually from detector space to world coordinate space and back) by using the transformations in the :code:`transform-schema` module.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/wcs/properties/steps:

  :entry:`steps`

  :soft:`Type:` :doc:`steps <steps>`. Required.

  

  A list of steps in the forward transformation from detector to
  world coordinates.
  
  The inverse transformation is determined automatically by
  reversing this list, and inverting each of the individual
  transforms according to the rules described in
  :ref:`inverse <http://stsci.edu/schemas/asdf/0.1.0/transform/transform/anyOf/0/properties/inverse>`.
  
  

.. only:: html

   :download:`Original schema in YAML <wcs.yaml>`
