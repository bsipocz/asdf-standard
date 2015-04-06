

.. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis:

axis: Specifies details about an axis in a WCS step.
====================================================

:soft:`Type:` object.

Specifies details about an axis in a WCS step.



A standard frame name should be used when appropriate, though
custom frame names may be used when necessary.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/type:

  :entry:`type`

  :soft:`Type:` any :soft:`from` ["celestial", "time", "spectral", "cartesian", "detector", "focal_plane", "custom"].

  

  The type of frame for this axis.  It must have one of the
  following values:
  
  -  :code:`celestial`: Celestial coordinates.  A :code:`celestial_type`
     property must also be given.
  
  -  :code:`time`: Time coordinate.  A :code:`time_scale` property must
     also be given.
  
  -  :code:`spectral`: Spectral coordinate.
  
  -  :code:`cartesian`: Cartesian coordinate.
  
  -  :code:`detector`: Native detector coordinate.
  
  -  :code:`focal_plane`: A coordinate in the focal plane.  Naturally,
     these coordinates will be instrument specific.
  
  -  :code:`custom`: A custom axis frame that is not one of the above.
     Additional information about the frame may be stored in additional
     properties as a non-standard extension.
  
  



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/celestial_type:

  :entry:`celestial_type`

  :soft:`Type:` any :soft:`from` ["FK4", "FK5", "Galactic", "ICRS"].

  

  If :code:`type` is "celestial", this property must be given.
  
  -  FK4: Celestial coordinates in the FK4 system.  :code:`equinox` and
     :code:`observation_time` may also be given.  :code:`name` should be
     :code:`ra` or :code:`dec`.
  
  -  FK5: Celestial coordinates in the FK5 system.  :code:`equinox` may
     also be given.  :code:`name` should be :code:`ra` or :code:`dec`.
  
  -  ICRS: Celestial coordinates in the ICRS system.  :code:`name`
     should be :code:`ra` or :code:`dec`.
  
  -  galactic: Galactic coordinates.  :code:`name` should be :code:`lon`
     or :code:`lat`.
  
  

  :soft:`Default:` "ICRS"



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/equinox:

  :entry:`equinox`

  :soft:`Type:` string.

  

  The equinox of the celestial frame.
  
  

  :soft:`Default:` "J2000"



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/observation_time:

  :entry:`observation_time`

  :soft:`Type:` string.

  

  The observation time of the celestial frame, if different from
  :code:`equinox`.
  
  



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/time_scale:

  :entry:`time_scale`

  :soft:`Type:` any :soft:`from` ["TAI", "TCB", "TCG", "TDB", "TT", "UT1", "UTC"].

  

  The time scale of the time axis.  Must be one of:
  
  -  TAI: International Atomic Time
  
  -  TCB: Barycentric Coordinate Time
  
  -  TCG: Geocentric Coordinate Time
  
  -  TDB: Barycentric Dynamical Time
  
  -  TT: Terrestrial Time
  
  -  UT1: Universal Time
  
  -  UTC: Coordinated Universal Time
  
  



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/spectral_type:

  :entry:`spectral_type`

  :soft:`Type:` any.

  

  TODO
  
  



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/name:

  :entry:`name`

  :soft:`Type:` string :soft:`or` any :soft:`from` ["ra", "dec", "lon", "lat", "x", "y", "z"].

  

  The name of the axis.  If the :code:`type` is multidimensional, such
  as "celestial", this name has meaning, and must correspond to
  it.  For example, for a celestial ICRS frame, it must be either
  "ra" or "dec".  Otherwise, it may be an arbitrary name for the
  axis.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/name/anyOf/0:

    :entry:`—`

    :soft:`Type:` string.

    

    



    .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/name/anyOf/1:

    :entry:`—`

    :soft:`Type:` any :soft:`from` ["ra", "dec", "lon", "lat", "x", "y", "z"].

    

    



  .. _http://stsci.edu/schemas/asdf/0.1.0/wcs/axis/properties/unit:

  :entry:`unit`

  :soft:`Type:` :doc:`unit <../unit/unit>`.

  

  The unit for the axis.
  
  

.. only:: html

   :download:`Original schema in YAML <axis.yaml>`
