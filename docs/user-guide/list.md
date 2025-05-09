# The List

The list type is a container type with a collection of homogeneous member types.

## Constructing the list

### Empty list

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

![empty list](./assets/images/list_head.png)

=== "SML"

    ``` sml linenums="1"
    hd(["My name ", "is ", "MNL"])
    ```

=== "Scala"

    ``` scala linenums="1"
    List("My name ", "is ", "MNL").head
    ```


### tail
![empty list](./assets/images/list_tail.png)

=== "SML"

    ``` sml linenums="1"
    tl(["My name ", "is ", "MNL"])
    ```

=== "Scala"

    ``` scala linenums="1"
    List("My name ", "is ", "MNL").tail
    ```


### append
![empty list](./assets/images/list_append.png)

=== "SML"

    ``` sml linenums="1"
    ("Hello, " :: ["My name ", "is ", "MNL"])
    ```

=== "Scala"

    ``` scala linenums="1"
    ("Hello, " :: List("My name ", "is ", "MNL"))
    ```


## Example

### Sum
![empty list](./assets/images/list_ex_sum.png)

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
