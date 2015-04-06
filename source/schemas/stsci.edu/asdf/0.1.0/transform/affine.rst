

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine:

affine: An affine transform.
============================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` object.

An affine transform.



Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/matrix:

    :entry:`matrix`

    :soft:`Type:` :doc:`ndarray <../core/ndarray>` :soft:`or` array :soft:`of` ( array :soft:`of` ( number ) *len* = 2 ) *len* = 2. Required.

    

    An array of size (*n* x *n*), where *n* is the number of axes,
    representing the linear transformation in an affine transform.
    
    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/matrix/anyOf/0:

      :entry:`—`

      :soft:`Type:` :doc:`ndarray <../core/ndarray>`.

      

      



      .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/matrix/anyOf/1:

      :entry:`—`

      :soft:`Type:` array :soft:`of` ( array :soft:`of` ( number ) *len* = 2 ) *len* = 2.

      

      

      :category:`Items:`



        .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/matrix/anyOf/1/items:

        :soft:`Type:` array :soft:`of` ( number ) *len* = 2.

        

        

        :category:`Items:`



          .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/matrix/anyOf/1/items/items:

          :soft:`Type:` number.

          

          



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/translation:

    :entry:`translation`

    :soft:`Type:` :doc:`ndarray <../core/ndarray>` :soft:`or` array :soft:`of` ( number ) *len* = 2.

    

    An array of size (*n*,), where  *n* is the number of axes,
    representing the translation in an affine transform.
    
    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/translation/anyOf/0:

      :entry:`—`

      :soft:`Type:` :doc:`ndarray <../core/ndarray>`.

      

      



      .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/translation/anyOf/1:

      :entry:`—`

      :soft:`Type:` array :soft:`of` ( number ) *len* = 2.

      

      

      :category:`Items:`



        .. _http://stsci.edu/schemas/asdf/0.1.0/transform/affine/allOf/1/properties/translation/anyOf/1/items:

        :soft:`Type:` number.

        

        

.. only:: html

   :download:`Original schema in YAML <affine.yaml>`
