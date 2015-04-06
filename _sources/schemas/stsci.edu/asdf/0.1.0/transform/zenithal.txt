

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/zenithal:

zenithal: Base class of all zenithal (or azimuthal) projections.
================================================================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` object.

Base class of all zenithal (or azimuthal) projections.



Zenithal projections are completely specified by defining the radius
as a function of native latitude, :math:`R_\theta`.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \arg(-y, x) \\
   R_\theta &= \sqrt{x^2 + y^2}

and the inverse (sky-to-pixel) is defined as:

.. math:: 

   x &= R_\theta \sin \phi \\
   y &= R_\theta \cos \phi



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/zenithal/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/zenithal/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/zenithal/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["pix2sky", "sky2pix"].

    

    

    :soft:`Default:` "pix2sky"

.. only:: html

   :download:`Original schema in YAML <zenithal.yaml>`
