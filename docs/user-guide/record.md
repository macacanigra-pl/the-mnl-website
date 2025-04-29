## Constructor
![workspace](assets/images/record_constructor.png){title="Record constructor"}

=== "SML"

    ``` sml linenums="1"
    {bool = false, str = "is", num = 0}
    ```

=== "Scala"

    ``` scala linenums="1"
    /* Scala doesn't have primitive type of 'Record' */
    ```

![workspace](assets/images/record_constructor_binding.png){title="record constructor - binding"}

=== "SML"

    ``` sml linenums="1"
    val record_constructor = {bool = false, str = "is", num = 0}
    ```

=== "Scala"

    ``` scala linenums="1"
    /* Scala doesn't have primitive type of 'Record' */
    ```

## Projection

![workspace](assets/images/record_projection.png){title="record projection"}

=== "SML"

    ``` sml linenums="1"
    (#str {bool = false, str = "is", num = 0})

    ```

=== "Scala"

    ``` scala linenums="1"
    /* Scala doesn't have primitive type of 'Record' */
    ```

![workspace](assets/images/record_projection_binding.png){title="record projection"}

=== "SML"

    ``` sml linenums="1"
    val record_constructor = {bool = false, str = "is", num = 0}
    val projection = (#str record_constructor)
    ```

=== "Scala"

    ``` scala linenums="1"
    /* Scala doesn't have primitive type of 'Record' */
    ```