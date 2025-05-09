# The Transpiler

MNL has its own transpiler called YAKI (Yet Another [K/T]Transpiler Interface), which transforms block-based programming languages into text-based languages such as SML and Scala. Beyond the transpiling, YAKI was able to write a typing derivation of MNL.

Right-click on the workspace and choose `Transpiler` to open the transpiler window. The combo box at the bottom allows users to select the target language.

![transpiler-window](./assets/images/transpiler_window.png)

/// caption
Fig. 1: YAKI
///


## Example: The Identity Function

??? Note "The Identity Function"
    :man_raising_hand: The identity function is a function that returns the input value.


![transpiler-block](./assets/images/transpiler_block_source.png)

/// caption
Fig. 2: The identity function
///

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

