

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

## Take two or more parameters

### Tuple
![workspace](assets/images/function_simul_two_params_tuple.png){title="tuple"}

### Record
![workspace](assets/images/function_simul_two_params_record.png){title="record"}