# The Compiler

MNL has its own compiler called YAKI (Yet Another [K/C]Compiler Interface), which transforms block-based programming languages into text-based languages such as SML and Scala. Beyond the transpiling, YAKI was able to write a typing derivation of MNL.

Choosing the target language via the select box in the 

![transpiler-window](./assets/images/transpiler_window.png)

/// caption
YAKI
///

![transpiler-block](./assets/images/transpiler_block_source.png)

## Target

=== "Typing Derivation"

    ![sum-list](./assets/images/typing_derivation.png)

=== "SML"

    ``` sml title="identity_function.sml" linenums="1"
    fun f_identity (a) = a
    ```

=== "Scala"

    ``` scala title="identity_function.scala" linenums="1"
    def f_identity [B] (a : B) : B = a 
    ```


??? Note "The Identity Function"
    :man_raising_hand: The identity function is a function that return the input value
