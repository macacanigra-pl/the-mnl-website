# The List

The list type is a container type with a collection of homogeneous member types. A list can be empty or non-empty.

## Constructing the list

### Empty list

Constructing the empty list block by removing all members in the input block toolbox [[&#9881;](overview.md#block-anatomy)]

![empty list](./assets/images/list_empty.png)

/// caption
Fig. 1: The empty list block
///

=== "SML"

    ``` sml linenums="1"
    []
    ```

=== "Scala"

    ``` scala linenums="1"
    List()
    ```


![empty list](./assets/images/list_empty_binding.png)

/// caption
Fig. 2: Connecting the empty list block to the variable block
///

=== "SML"

    ``` sml linenums="1"
    val list_constructor = []
    ```

=== "Scala"

    ``` scala linenums="1"
    val list_constructor = List()
    ```


### Non-empty list

The inhabitants of the list can be added or removed using the input block toolbox.

![not empty list](./assets/images/list_non_empty.png)

/// caption
Fig. 3: Constructing the non-empty list block
///

=== "SML"

    ``` sml linenums="1"
    ["my name ", "is ", "MNL"]
    ```

=== "Scala"

    ``` scala linenums="1"
    List("my name ", "is ", "MNL")
    ```


![not empty list](./assets/images/list_non_empty_binding.png)

/// caption
Fig. 4: Connecting the non-empty list block to the variable block
///

=== "SML"

    ``` sml linenums="1"
    val list_constructor = ["my name ", "is ", "MNL"]
    ```

=== "Scala"

    ``` scala linenums="1"
    val list_constructor = List("my name ", "is ", "MNL")
    ```

## Operator

### is empty

To check whether the list is empty or not. Returning true when the is empty, otherwise is false.

![is empty - true](./assets/images/list_is_empty_true.png)

/// caption
Fig. 5: The is-empty block operator with the empty list block
///

=== "SML"

    ``` sml linenums="1"
    val list_constructor = null([])
    ```

=== "Scala"

    ``` scala linenums="1"
    val list_constructor = List().isEmpty
    ```

![is empty - false](./assets/images/list_is_empty_false.png)

/// caption
Fig. 6: The is-empty block operator with the non-empty list block
///

=== "SML"

    ``` sml linenums="1"
    val list_constructor = null([])
    ```

=== "Scala"

    ``` scala linenums="1"
    val list_constructor = List().isEmpty
    ```

### head

Returning the first inhabitant of the list.

![empty list](./assets/images/list_head.png)

/// caption
Fig. 7: The head list operator block
///

=== "SML"

    ``` sml linenums="1"
    hd(["My name ", "is ", "MNL"])
    ```

=== "Scala"

    ``` scala linenums="1"
    List("My name ", "is ", "MNL").head
    ```


### tail

Returning the inhabitants of the list, starting from the second to the last inhabitant.

![empty list](./assets/images/list_tail.png)

/// caption
Fig. 8: The tail list operator block
///

=== "SML"

    ``` sml linenums="1"
    tl(["My name ", "is ", "MNL"])
    ```

=== "Scala"

    ``` scala linenums="1"
    List("My name ", "is ", "MNL").tail
    ```

### append

Insert a new inhabitant into the list and put it into the first position.

![empty list](./assets/images/list_append.png)

/// caption
Fig. 9: The append list operator block
///

=== "SML"

    ``` sml linenums="1"
    ("Hello, " :: ["My name ", "is ", "MNL"])
    ```

=== "Scala"

    ``` scala linenums="1"
    ("Hello, " :: List("My name ", "is ", "MNL"))
    ```

![empty list](./assets/images/list_append_ex_1.png)

/// caption
Fig. 10: The append a new inhabitant and bind to a variable block.
///

=== "SML"

    ``` sml linenums="1"
    val my_name_is_mnl = ["My name", "is", "MNL"]
    val hello = ("Hello, " :: my_name_is_mnl)
    ```

=== "Scala"

    ``` scala linenums="1"
    val my_name_is_mnl = List("My name", "is", "MNL")
    val hello = ("Hello, " :: my_name_is_mnl)
    ```


## Example

### Sum

![empty list](./assets/images/list_ex_sum.png)

/// caption
Fig. 11: The head list operator block
///

=== "SML"

    ``` sml linenums="1"
    fun sum_list (list_a) = if null(list_a)
      then
        0
      else
        (hd(list_a)  + sum_list(tl(list_a)))

    val sum_list_application = sum_list([17, 2, 200, 4])
    ```

=== "Scala"

    ``` scala linenums="1"
    def sum_list (list_a: List[Float]) : Float = if (list_a.isEmpty)
      then
        0
      else
        ((list_a.head)  + sum_list((list_a.tail)))

    val sum_list_application = sum_list(List(17, 2, 200, 4))
    ```
