

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/transform:

transform: A generic type used to mark where other transforms are accepted.
===========================================================================

:soft:`Type:` object :soft:`or` any.

A generic type used to mark where other transforms are accepted.



These objects are designed to be nested in arbitrary ways to build up transformation pipelines out of a number of low-level pieces.



:category:`Any of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/transform/anyOf/0:

  :entry:`—`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/transform/anyOf/0/properties/name:

    :entry:`name`

    :soft:`Type:` string.

    

    A user-friendly name for the transform, to give it extra
    meaning.
    
    



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/transform/anyOf/0/properties/domain:

    :entry:`domain`

    :soft:`Type:` array :soft:`of` ( :doc:`domain <domain>` ).

    

    The domain (range of valid inputs) to the transform.
    Each entry in the list corresponds to an input dimension.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/0.1.0/transform/transform/anyOf/0/properties/domain/items:

      :soft:`Type:` :doc:`domain <domain>`.

      

      



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/transform/anyOf/0/properties/inverse:

    :entry:`inverse`

    :soft:`Type:` :doc:`transform <transform>`.

    

    Explicitly sets the inverse transform of this transform.
    
    If the transform has a direct analytic inverse, this
    property is usually not necessary, as the ASDF-reading tool
    can provide it automatically.
    
    



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/transform/anyOf/1:

  :entry:`—`

  :soft:`Type:` any.

  

  

.. only:: html

   :download:`Original schema in YAML <transform.yaml>`
