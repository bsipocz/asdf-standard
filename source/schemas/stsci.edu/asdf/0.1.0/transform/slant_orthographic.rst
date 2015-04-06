

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/slant_orthographic:

slant_orthographic: The slant orthographic projection.
======================================================

:soft:`Type:` :doc:`zenithal <zenithal>`.

The slant orthographic projection.



Corresponds to the :code:`SIN` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/0.1.0/transform/zenithal>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = \cos^{-1}\left(\frac{\pi}{180^{\circ}}R_\theta\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta = \frac{180^{\circ}}{\pi}\cos \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



.. only:: html

   :download:`Original schema in YAML <slant_orthographic.yaml>`
