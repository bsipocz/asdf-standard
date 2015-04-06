

.. _http://stsci.edu/schemas/asdf/0.1.0/transform/concatenate:

concatenate: Send axes to different subtransforms.
==================================================

:soft:`Type:` :doc:`transform <transform>` :soft:`and` any.

Send axes to different subtransforms.



Transforms a set of separable inputs by splitting the axes apart,
sending them through the given subtransforms in parallel, and
finally concatenating the subtransform output axes back together.

The input axes are assigned to each subtransform in order.  If the
number of input axes is unequal to the sum of the number of input
axes of all of the subtransforms, that is considered an error case.

The output axes from each subtransform are appended together to make
up the resulting output axes.

For example, given 5 input axes, and 3 subtransforms with the
following orders:


#. transform A: 2 in -> 2 out

#. transform B: 1 in -> 2 out

#. transform C: 2 in -> 1 out

The transform is performed as follows:

.. code:: 

   :    i0    i1       i2       i3    i4
   :    |     |        |        |     |
   :  +---------+ +---------+ +----------+
   :  |    A    | |    B    | |    C     |
   :  +---------+ +---------+ +----------+
   :    |     |     |     |        |
   :    o0    o1    o2    o3       o4

If reordering of the input or output axes is required, use in series
with the :code:`remap_axes` transform.

Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/concatenate/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform <transform>`.

  

  



  .. _http://stsci.edu/schemas/asdf/0.1.0/transform/concatenate/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

The example in the description::

  !transform/concatenate
    forward:
      - !transform/generic
        n_inputs: 2
        n_outputs: 2
      - !transform/generic
        n_inputs: 1
        n_outputs: 2
      - !transform/generic
        n_inputs: 2
        n_outputs: 1
  

.. only:: html

   :download:`Original schema in YAML <concatenate.yaml>`
