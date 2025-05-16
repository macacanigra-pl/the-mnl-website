# Tuple

The tuple type is a container type with a collection of heterogeneous inhabitant types. A tuple size is fixed and can not be empty.

## Constructor

![workspace](assets/images/tuple_constructor.png){title="Tuple constructor"}

/// caption
Fig. 1: Tuple constructor
///


=== "SML"

    ``` sml linenums="1"
    (true, "is", 1)
    ```

=== "Scala"

    ``` scala linenums="1"
    (true, "is", 1)
    ```

![workspace](assets/images/tuple_constructor_binding.png){title="Binding a tuple"}

/// caption
Fig. 2: Binding a tuple
///

=== "SML"

    ``` sml linenums="1"
    val tuple_constructor = (true, "is", 1)
    ```

=== "Scala"

    ``` scala linenums="1"
    val tuple_constructor = (true, "is", 1)
    ```

## Projection

Projection is an operator that gets one tuple inhabitant at a specific location.

![workspace](assets/images/tuple_projection.png){title="Tuple projection"}

/// caption
Fig. 3: Tuple projection
///

=== "SML"

    ``` sml linenums="1"
    val tuple_constructor = (true, "is", 1)
    val projection = (#1 tuple_constructor)
    ```

=== "Scala"

    ``` scala linenums="1"
    val tuple_constructor = (true, "is", 1)
    val projection = (tuple_constructor(1))
    ```