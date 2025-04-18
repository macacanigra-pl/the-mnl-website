---
tags:
  - Transpiler
  - YAKI
---


## Choose the target
<!-- ![transpiler-window](./assets/images/transpiler_window.png) -->
<img src="./assets/images/transpiler_window.png" width="40%" height="40%">

<!-- ![transpiler-block](./assets/images/transpiler_block_source.png) -->
<img src="./assets/images/transpiler_block_source.png" width="30%" height="30%">

## Target

=== "Formalization"

    ![sum-list](./assets/images/transpiler.png)

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
