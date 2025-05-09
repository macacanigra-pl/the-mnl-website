# The Function

A function is an expression with a function type and has a name (binding with a name). Lambda is an expression with a function type with no name (anonymous function).

## The Lambda Block

![workspace](assets/images/lambda.png){title="Lambda"}

/// caption
Fig. 1: The lambda block and binding.
///

=== "SML"

    ``` sml linenums="1"
    val mnl_say = fn (hello) => ("MNL: " ^ hello)
    ```

=== "Scala"

    ``` scala linenums="1"
    val mnl_say = (hello : String) => ("MNL: " + hello)
    ```

## The Function block

MNL simplifies the construction by binding the lambda block with a name in one special declaration block called a function block.

![workspace](assets/images/first_class_function_1.png){title="First class function"}

/// caption
Fig. 2: The function block
///

=== "SML"

    ``` sml linenums="1"
    fun greetings () = "Hello there"
    val say_it = greetings()
    ```

=== "Scala"

    ``` scala linenums="1"
    def greetings () : String = "Hello there"
    val say_it = greetings()
    ```

## Example

### Tail Function

![workspace](assets/images/tail_function.png){title="Tail function"}

/// caption
Fig. 3: The tail function
///

=== "SML"

    ``` sml linenums="1"
    fun tail_function (n) = if (n <= 1)
        then
            1
        else
	        (n * tail_function((n - 1)))
    ```

=== "Scala"

    ``` scala linenums="1"
    def tail_function (n: Float) : Float = if (n <= 1)
        then
            1
        else
            (n * tail_function((n - 1)))
    ```

### Two or more parameters

The core language of MNL is the lambda calculus, which takes one parameter. However, MNL can take two or more inputs as parameters using a tuple or a record. The examples below show how to group two inputs as one parameter.

#### Tuple

![workspace](assets/images/function_simul_two_params_tuple.png){title="tuple"}

/// caption
Fig. 4: A tuple as the function parameter
///

=== "SML"

    ``` sml linenums="1"
    (* SML does not support type inference for a tuple as a parameter. 
    Other ML languages may support the syntax below. *)
    fun greetings (tpl) = (#1 (tpl)) ^ (#2 (tpl))
    val greetings_1 = greetings(("Hello ", "World!"))
    val greetings_2 = greetings(("World!", "Hello "))
    ```

=== "Scala"

    ``` scala linenums="1"
    /* the first item name/ index is 0 in scala */
    def greetings (tpl: (String, String)) : String = ((tpl(0)) + (tpl(1)))
    val greetings_1 = greetings(("Hello ", "World!"))
    val greetings_2 = greetings(("World!", "Hello "))
    ```

#### Record

![workspace](assets/images/function_simul_two_params_record.png){title="record"}

/// caption
Fig. 5: A record as the function parameter
///

=== "SML"

    ``` sml linenums="1"
     (* SML does not support type inference for a record as a parameter. 
    Other ML languages may support the syntax below. *)
    fun greetings (rcd) = ((#a (rcd)) ^ (#b (rcd)))
    val greetings_1 = greetings({a = "Hello ", b = "World!"})
    val greetings_2 = greetings({b = "World!", a = "Hello "})
    ```

=== "Scala"

    ``` scala linenums="1"
    def greetings (rcd: record of {a : String and b : String}) : String = (/* Scala doesn't have primitive type of 'Record' */ + /* Scala doesn't have primitive type of 'Record' */)
    val greetings_1 = greetings(/* Scala doesn't have primitive type of 'Record' */)
    val greetings_2 = greetings(/* Scala doesn't have primitive type of 'Record' */)
    ```
