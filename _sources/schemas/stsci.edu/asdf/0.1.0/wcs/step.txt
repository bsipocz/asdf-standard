

.. _http://stsci.edu/schemas/asdf/0.1.0/wcs/step:

step: Describes a single step of a WCS transform pipeline.
==========================================================

:soft:`Type:` object.

Describes a single step of a WCS transform pipeline.





:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/step/properties/name:

  :entry:`name`

  :soft:`Type:` string.

  

  The name of this step on the WCS transform pipeline.  This name
  may be used by a library to allow the user to say "transform
  from pixel space to the focal plane" without performing the
  entire WCS pipeline.
  
  



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/step/properties/axes:

  :entry:`axes`

  :soft:`Type:` array :soft:`of` ( :doc:`axis <axis>` ).

  

  A description of each of the input axes for this step.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/step/properties/axes/items:

    :soft:`Type:` :doc:`axis <axis>`.

    

    



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/step/properties/transform:

  :entry:`transform`

  :soft:`Type:` :doc:`transform <../transform/transform>`.

  

  The transform from this step to the next one.  The
  last step in a WCS should not have a transform, but
  exists only to describe the frames and units of the
  final output axes.
  
  

.. only:: html

   :download:`Original schema in YAML <step.yaml>`
