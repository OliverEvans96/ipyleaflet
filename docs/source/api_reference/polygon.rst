Polygon/Multipolygon
====================

Example Polygon
---------------

.. jupyter-execute::

    from ipyleaflet import Map, Polygon

    polygon = Polygon(
        locations=[(42, -49), (43, -49), (43, -48)],
        color="green",
        fill_color="green"
    )

    m = Map(center=(42.5531, -48.6914), zoom=6)
    m.add_layer(polygon);

    m


Example Polygon with hole
-------------------------

.. jupyter-execute::

  from ipyleaflet import Map, Polygon

  hole_polygon = Polygon(
      locations= [[(37, -109.05),(41, -109.03),(41, -102.05),(37, -102.04)],
      [(37.29, -108.58),(40.71, -108.58),(40.71, -102.50),(37.29, -102.50)]],

      color="green",
      fill_color="green"
  )

  m = Map(center=(37.5531, -109.6914), zoom=5)
  m.add_layer(hole_polygon);

  m


Example Multipolygon
--------------------

.. jupyter-execute::

    from ipyleaflet import Map, Polygon

    multipolygon = Polygon(
            locations=[[(42, -49), (43, -49), (43, -48)],[(44,-49),(43, -50),(44,-50)]],
            color="green",
            fill_color="green"
        )

    m = Map(center=(42.5531, -48.6914), zoom=6)
    m.add_layer(multipolygon);

    m


Attributes
----------

=============    ================   ===
Attribute        Default Value      Doc
=============    ================   ===
locations        []                 List of points of the polygon
stroke           True               Set it to `False` to disable borders
color            "#0033FF"          Stroke color
opacity          1.0                Stroke opacity
weight           5                  Stroke width in pixels
fill             True               Whether to fill the polygon or not
fill_color       "#0033FF"
fill_opacity     0.2
dash_array
line_cap         "round"
line_join        "round"
=============    ================   ===
