

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/polynomial:

polynomial: A Polynomial model.
===============================

:soft:`Type:` object.

A Polynomial model.



A polynomial model represented by its coefficients stored in
an ndarray of shape :math:`(n+1)` for univariate polynomials or :math:`(n+1, n+1)`
for polynomials with 2 variables, where :math:`n` is the highest total degree
of the polynomial.

.. math:: 

   P = \sum_{i, j=0}^{i+j=n}c_{ij} * x^{i} * y^{j}

Invertibility: This transform is not automatically invertible.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/polynomial/properties/coefficients:

  :entry:`coefficients`

  :soft:`Type:` :doc:`ndarray <../core/ndarray>` :soft:`or` array. Required.

  

  An array with coefficients.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/polynomial/properties/coefficients/anyOf/0:

    :entry:`—`

    :soft:`Type:` :doc:`ndarray <../core/ndarray>`.

    

    



    .. _http://stsci.edu/schemas/asdf/0.1.0/transform/polynomial/properties/coefficients/anyOf/1:

    :entry:`—`

    :soft:`Type:` array.

    

    

    :category:`Items:`

:category:`Examples:`

:math:`P = 1.2 + 0.3 * x + 56.1 * x^{2}`::

  !transform/polynomial
    coefficients: !core/ndarray
                    [1.2, 0.3, 56.1]
  

:math:`P = 1.2 + 0.3 * x + 3 * x * y + 2.1 * y^{2}`::

  !transform/polynomial
    coefficients: !core/ndarray
                    [[1.2, 0.0, 2.1],
                     [0.3, 3.0, 0.0],
                     [0.0, 0.0, 0.0]]
  

.. only:: html

   :download:`Original schema in YAML <polynomial.yaml>`
