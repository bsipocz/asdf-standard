

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/domain:

domain: Defines the domain of an input axis.
============================================

:soft:`Type:` any.

Defines the domain of an input axis.



Describes the range of acceptable input values to a particular axis of a transform.



:category:`Examples:`

The domain :code:`[0, 1)`.::

  !transform/domain
    lower: 0
    upper: 1
    includes_lower: true
  

.. only:: html

   :download:`Original schema in YAML <domain.yaml>`
