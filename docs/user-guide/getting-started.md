## Just Drag, Drop, and Attach the block

![workspace](assets/images/drag_light.png#only-light)
![workspace](assets/images/drag_dark.png#only-dark)


## Variable
![workspace](assets/images/variable_binding.png){title="Variable binding"}

=== "SML"

    ``` sml linenums="1"
    val variable = "Hello World!"
    ```

=== "Scala"

    ``` scala linenums="1"
    val variable = "Hello World!"
    ```

## Operator

### Unary
![workspace](assets/images/unary_operator_boolean.png){title="Boolean Operator Not"}

=== "SML"

    ``` sml linenums="1"
    val unary_operator = (not true)
    ```

=== "Scala"

    ``` scala linenums="1"
    val unary_operator = (!true)
    ```

### Binary
![workspace](assets/images/binary_operator_arithmetic.png){title="Arithmetic Operator"}

=== "SML"

    ``` sml linenums="1"
    val arithmetic = (111 + 222)
    ```

=== "Scala"

    ``` scala linenums="1"
    val arithmetic = (111 + 222)
    ```


## Selection
![workspace](assets/images/selection.png){title="Selection"}

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
![workspace](assets/images/sequence_light.png#only-light)
![workspace](assets/images/sequence_dark.png#only-dark)

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
![workspace](assets/images/pattern_matching.png){title="Pattern Matching"}

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
![workspace](assets/images/let_in.png){title="Pattern Matching"}

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
