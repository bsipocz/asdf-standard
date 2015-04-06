

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/gnomonic:

gnomonic: The gnomonic projection.
==================================

:soft:`Type:` :doc:`zenithal <zenithal>`.

The gnomonic projection.



Corresponds to the :code:`TAN` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/0.1.0/transform/zenithal>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = \tan^{-1}\left(\frac{180^{\circ}}{\pi R_\theta}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta = \frac{180^{\circ}}{\pi}\cot \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



.. only:: html

   :download:`Original schema in YAML <gnomonic.yaml>`
