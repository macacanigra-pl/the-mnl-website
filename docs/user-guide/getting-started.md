# Getting Started

## Just Drag, Drop, and Attach the block

<div class="annotate" markdown>

To start constructing a program in MNL, drag a block from the toolbox to the playground area and attach it to another block.
There is a main block (1) acts as the parent block. The main block will hold declaration block only.

</div>

1.  :man_raising_hand: The black block with MNL on the top.

![workspace](assets/images/drag_light.png#only-light){title="Drag, drop, and attach the block" loading=lazy }
![workspace](assets/images/drag_dark.png#only-dark){title="Drag, drop, and attach the block" loading=lazy }

/// caption
Drag, drop, and attach the block
///


## Variable

Creating a variable 
![workspace](assets/images/variable_binding.png){title="Variable binding" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    val variable_in_MNL = "MNL is easy to learn"
    ```

=== "Scala"

    ``` scala linenums="1"
    val variable_in_MNL = "MNL is easy to learn"
    ```

## Operator

### Unary
![workspace](assets/images/unary_operator_boolean.png){title="Boolean Operator Not" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    (not false)
    ```

=== "Scala"

    ``` scala linenums="1"
    (!false)
    ```

![workspace](assets/images/unary_operator_boolean_binding.png){title="Boolean Operator Not - binding" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    val unary_operator = (not false)
    ```

=== "Scala"

    ``` scala linenums="1"
    val unary_operator = (!false)
    ```

### Binary
![workspace](assets/images/binary_operator_arithmetic.png){title="Arithmetic Operator" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    (111 + 222)
    ```

=== "Scala"

    ``` scala linenums="1"
    (111 + 222)
    ```

![workspace](assets/images/binary_operator_binding.png){title="Arithmetic Operator - binding" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    fun increment (n) = (1 + n)
    val three = increment(2)
    ```

=== "Scala"

    ``` scala linenums="1"
    def increment (n: Float) : Float = (1 + n)
    val three = increment(2)
    ```


## Selection
![workspace](assets/images/selection.png){title="Selection" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    fun the_greater (pair) = if ((#1 pair) < (#2 pair))
      then
        (#2 pair)
      else
        (#1 pair)
    val two_or_three = the_greater((2, 3))
    ```

=== "Scala"

    ``` scala linenums="1"
    def the_greater (pair: (Float, Float)) : Float = if ((pair(1)) < (pair(2)))
      then
        (pair(2))
      else
        (pair(1))
    val two_or_three = the_greater((2, 3))
    ```


## Sequence
![workspace](assets/images/sequence_light.png#only-light){title="Sequence" loading=lazy }
![workspace](assets/images/sequence_dark.png#only-dark){title="Sequence" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    val sequence = (
        "Hi, there!";
        "I am MNL"
      )
    ```

=== "Scala"

    ``` scala linenums="1"
    val sequence = (() =>{
        "Hi, there!"
        "I am MNL"
      })()
    ```

## Pattern Matching
![workspace](assets/images/pattern_matching.png){title="Pattern Matching" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    fun translator_good_morning (lang_code) = case lang_code
      of "en" => "Good Morning"
      | "de" => "Guten Morgen"
      | "jp" => "おはよう"
      | "id" => "Selamat Pagi"
      |  _   => "Unknown"

    val greetings = translator_good_morning("de")
    ```

=== "Scala"

    ``` scala linenums="1"
    def translator_good_morning (lang_code: String) : String = lang_code match
      case "en" => "Good Morning"
      case "de" => "Guten Morgen"
      case "jp" => "おはよう"
      case "id" => "Selamat Pagi"
      case  _   => "Unknown"

    val greetings = translator_good_morning("de")
    ```

## Let-in
![workspace](assets/images/let_in.png){title="Pattern Matching" loading=lazy }

=== "SML"

    ``` sml linenums="1"
    val let_in = let
        val hello = "Hello "
        fun speech (name) = (hello ^ name)
      in
        speech("MNL")
      end
    ```

=== "Scala"

    ``` scala linenums="1"
    val let_in = (() => {
      val hello = "Hello "
      def speech (name: String) : String = (hello + name)

      speech("MNL")
    })()
    ```
