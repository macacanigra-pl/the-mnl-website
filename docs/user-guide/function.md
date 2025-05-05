# The Function

## Function

![workspace](assets/images/first_class_function_1.png){title="First class function"}

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



## Lambda

![workspace](assets/images/lambda.png){title="Lambda"}

=== "SML"

    ``` sml linenums="1"
    val mnl_say = fn (hello) => ("MNL: " ^ hello)
    ```

=== "Scala"

    ``` scala linenums="1"
    val mnl_say = (hello : String) => ("MNL: " + hello)
    ```

## Tail Function

![workspace](assets/images/tail_function.png){title="Tail function"}

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

## Take two or more parameters

### Tuple

![workspace](assets/images/function_simul_two_params_tuple.png){title="tuple"}

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

### Record

![workspace](assets/images/function_simul_two_params_record.png){title="record"}

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
