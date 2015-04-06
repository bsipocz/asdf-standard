

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/stereographic:

stereographic: The stereographic projection.
============================================

:soft:`Type:` :doc:`zenithal <zenithal>`.

The stereographic projection.



Corresponds to the :code:`STG` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/0.1.0/transform/zenithal>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = 90^{\circ} - 2 \tan^{-1}\left(\frac{\pi R_\theta}{360^{\circ}}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta = \frac{180^{\circ}}{\pi}\frac{2 \cos \theta}{1 + \sin \theta}

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



.. only:: html

   :download:`Original schema in YAML <stereographic.yaml>`
