# Tuple

The tuple type is a container type with a collection of heterogeneous member types. A tuple size is fixed and can not be empty.

## Constructor

![workspace](assets/images/tuple_constructor.png){title="Tuple constructor"}

=== "SML"

    ``` sml linenums="1"
    (true, "is", 1)
    ```

=== "Scala"

    ``` scala linenums="1"
    (true, "is", 1)
    ```

![workspace](assets/images/tuple_constructor_binding.png){title="Tuple constructor - binding"}

=== "SML"

    ``` sml linenums="1"
    val tuple_constructor = (true, "is", 1)
    ```

=== "Scala"

    ``` scala linenums="1"
    val tuple_constructor = (true, "is", 1)
    ```

## Projection

![workspace](assets/images/tuple_projection.png){title="Tuple projection"}

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