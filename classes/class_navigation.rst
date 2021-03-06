:github_url: hide

.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the Navigation.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_Navigation:

Navigation
==========

**Inherits:** :ref:`Spatial<class_Spatial>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Mesh-based navigation and pathfinding node.

Description
-----------

Provides navigation and pathfinding within a collection of :ref:`NavigationMesh<class_NavigationMesh>`\ es. These will be automatically collected from child :ref:`NavigationRegion<class_NavigationRegion>` nodes. In addition to basic pathfinding, this class also assists with aligning navigation agents with the meshes they are navigating on.

Properties
----------

+-------------------------------+---------------------------------------------------------------------------------+------------------------+
| :ref:`float<class_float>`     | :ref:`cell_size<class_Navigation_property_cell_size>`                           | ``0.3``                |
+-------------------------------+---------------------------------------------------------------------------------+------------------------+
| :ref:`float<class_float>`     | :ref:`edge_connection_margin<class_Navigation_property_edge_connection_margin>` | ``5.0``                |
+-------------------------------+---------------------------------------------------------------------------------+------------------------+
| :ref:`Vector3<class_Vector3>` | :ref:`up_vector<class_Navigation_property_up_vector>`                           | ``Vector3( 0, 1, 0 )`` |
+-------------------------------+---------------------------------------------------------------------------------+------------------------+

Methods
-------

+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>`                       | :ref:`get_closest_point<class_Navigation_method_get_closest_point>` **(** :ref:`Vector3<class_Vector3>` to_point **)** const                                                                                                    |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>`                       | :ref:`get_closest_point_normal<class_Navigation_method_get_closest_point_normal>` **(** :ref:`Vector3<class_Vector3>` to_point **)** const                                                                                      |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`RID<class_RID>`                               | :ref:`get_closest_point_owner<class_Navigation_method_get_closest_point_owner>` **(** :ref:`Vector3<class_Vector3>` to_point **)** const                                                                                        |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>`                       | :ref:`get_closest_point_to_segment<class_Navigation_method_get_closest_point_to_segment>` **(** :ref:`Vector3<class_Vector3>` start, :ref:`Vector3<class_Vector3>` end, :ref:`bool<class_bool>` use_collision=false **)** const |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`RID<class_RID>`                               | :ref:`get_rid<class_Navigation_method_get_rid>` **(** **)** const                                                                                                                                                               |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PackedVector3Array<class_PackedVector3Array>` | :ref:`get_simple_path<class_Navigation_method_get_simple_path>` **(** :ref:`Vector3<class_Vector3>` start, :ref:`Vector3<class_Vector3>` end, :ref:`bool<class_bool>` optimize=true **)** const                                 |
+-----------------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Property Descriptions
---------------------

.. _class_Navigation_property_cell_size:

- :ref:`float<class_float>` **cell_size**

+-----------+----------------------+
| *Default* | ``0.3``              |
+-----------+----------------------+
| *Setter*  | set_cell_size(value) |
+-----------+----------------------+
| *Getter*  | get_cell_size()      |
+-----------+----------------------+

----

.. _class_Navigation_property_edge_connection_margin:

- :ref:`float<class_float>` **edge_connection_margin**

+-----------+-----------------------------------+
| *Default* | ``5.0``                           |
+-----------+-----------------------------------+
| *Setter*  | set_edge_connection_margin(value) |
+-----------+-----------------------------------+
| *Getter*  | get_edge_connection_margin()      |
+-----------+-----------------------------------+

----

.. _class_Navigation_property_up_vector:

- :ref:`Vector3<class_Vector3>` **up_vector**

+-----------+------------------------+
| *Default* | ``Vector3( 0, 1, 0 )`` |
+-----------+------------------------+
| *Setter*  | set_up_vector(value)   |
+-----------+------------------------+
| *Getter*  | get_up_vector()        |
+-----------+------------------------+

Defines which direction is up. By default, this is ``(0, 1, 0)``, which is the world's "up" direction.

Method Descriptions
-------------------

.. _class_Navigation_method_get_closest_point:

- :ref:`Vector3<class_Vector3>` **get_closest_point** **(** :ref:`Vector3<class_Vector3>` to_point **)** const

Returns the point closest to the provided ``to_point`` on the navigation mesh surface.

----

.. _class_Navigation_method_get_closest_point_normal:

- :ref:`Vector3<class_Vector3>` **get_closest_point_normal** **(** :ref:`Vector3<class_Vector3>` to_point **)** const

Returns the normal for the point returned by :ref:`get_closest_point<class_Navigation_method_get_closest_point>`.

----

.. _class_Navigation_method_get_closest_point_owner:

- :ref:`RID<class_RID>` **get_closest_point_owner** **(** :ref:`Vector3<class_Vector3>` to_point **)** const

Returns the owner region RID for the point returned by :ref:`get_closest_point<class_Navigation_method_get_closest_point>`.

----

.. _class_Navigation_method_get_closest_point_to_segment:

- :ref:`Vector3<class_Vector3>` **get_closest_point_to_segment** **(** :ref:`Vector3<class_Vector3>` start, :ref:`Vector3<class_Vector3>` end, :ref:`bool<class_bool>` use_collision=false **)** const

Returns the closest point between the navigation surface and the segment.

----

.. _class_Navigation_method_get_rid:

- :ref:`RID<class_RID>` **get_rid** **(** **)** const

----

.. _class_Navigation_method_get_simple_path:

- :ref:`PackedVector3Array<class_PackedVector3Array>` **get_simple_path** **(** :ref:`Vector3<class_Vector3>` start, :ref:`Vector3<class_Vector3>` end, :ref:`bool<class_bool>` optimize=true **)** const

Returns the path between two given points. Points are in local coordinate space. If ``optimize`` is ``true`` (the default), the agent properties associated with each :ref:`NavigationMesh<class_NavigationMesh>` (radius, height, etc.) are considered in the path calculation, otherwise they are ignored.

