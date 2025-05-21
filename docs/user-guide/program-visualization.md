# Program Visualisation

MNL features a program visualization tool called Tarsius. Tarsius was designed specifically for program visualization, which means that all evaluations are conducted within a visual workspace. This approach differs from traditional text-based programming languages, where it can be challenging to illustrate function values or the process of function application (beta reduction). Tarsius can visually display both the function value and all the steps in the beta reduction process during substitution and computation.

## The Function Value

When the expression block type is `function`, users can view the contents of the function value by right-clicking on the block and selecting `Function Value` from the block menu.

![workspace](assets/images/function_value_menu_dark.png#only-dark)
![workspace](assets/images/function_value_menu_light.png#only-light)

/// caption
Fig. 1: The function value's menu
///

![workspace](assets/images/function_value_window_dark.png#only-dark)
![workspace](assets/images/function_value_window_light.png#only-light)

/// caption
Fig. 2: The content of function's value
///

## Beta Reduction

Users can display the beta reduction process by right-clicking on the application block and selecting `Beta Reduction`. In the beta reduction window, they will see the substitution steps arranged sequentially from top to bottom, along with their corresponding values.

 ![workspace](assets/images/beta_reduction_menu_dark.png#only-dark)
 ![workspace](assets/images/beta_reduction_menu_light.png#only-light)

/// caption
Fig. 3: The beta reduction's menu
///

 ![workspace](assets/images/beta_reduction_window_dark.png#only-dark)
 ![workspace](assets/images/beta_reduction_window_light.png#only-light)

/// caption
Fig. 4: Beta reduction
///
