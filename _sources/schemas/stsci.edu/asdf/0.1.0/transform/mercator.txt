

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/mercator:

mercator: The Mercator projection.
==================================

:soft:`Type:` :doc:`cylindrical <cylindrical>`.

The Mercator projection.



Corresponds to the :code:`MER` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= x \\
   \theta &= 2 \tan^{-1}\left(e^{y \pi / 180^{\circ}}\right)-90^{\circ}

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= \phi \\
   y &= \frac{180^{\circ}}{\pi}\ln \tan \left(\frac{90^{\circ} + \theta}{2}\right)

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



.. only:: html

   :download:`Original schema in YAML <mercator.yaml>`
