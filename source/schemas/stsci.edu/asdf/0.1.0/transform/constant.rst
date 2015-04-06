

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/constant:

constant: A transform that takes no inputs and always outputs a constant value.
===============================================================================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` object.

A transform that takes no inputs and always outputs a constant value.



Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform, which always outputs zero values.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/constant/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/constant/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/constant/allOf/1/properties/value:

    :entry:`value`

    :soft:`Type:` number. Required.

    

    

.. only:: html

   :download:`Original schema in YAML <constant.yaml>`
