# Type Suggestion

One of the MNL capability is type suggestion. MNL will show the suggestion type by coloring the rounded-box near to the input notch.
 
Initially, MNL will color the suggestion box with any type color (dark silver), or when the type is fixed, then the color is based on it.

![type-suggestion](./assets/images/type_suggestion_1.png){title="The incomplete block"}

/// caption
Fig. 1: Suggestion type on the incomplete block
///

<div class="annotate" markdown>

However, when the block has some attached input (The partially completed block (1) ), MNL will construct the type based on the type constraint rule and update the suggestion box color. The example below shows the color of suggestion box on the input notch.

</div>

1.  :man_raising_hand: The partially completed block is a block with some attached input blocks, but not all input notches have connected with the input block.

![type-suggestion](./assets/images/type_suggestion_2.png){title="The partially completed block"}

/// caption

///

![type-suggestion](./assets/images/type_suggestion_3.png){title="The partially completed block"}

/// caption
Fig. 2: The partially completed block
///

<div class="annotate" markdown>

When the block is complete, user can check whether the input block complies with the typing rule. For example, the completed block below, the input block attached to the otherwise input, does not comply with the typing rule. The typing rule required the block with the green color (2), but found the block with the yellow color (3).

</div>

1.  :man_raising_hand: The completed block is a block with all input notches have connected to the input block.
2.  :man_raising_hand: The green color is the color for the type string.
3.  :man_raising_hand: The yellow color is the color for the type number.

![type-suggestion](./assets/images/type_suggestion_4.png){title="The completed block"}

/// caption
Fig. 3: The completed block
/// 

When the type constraint builder can't find the type from the attached input block but the block has parent block, it will infer the type from the parent block.

![type-suggestion](./assets/images/type_suggestion_5.png){title="Infer from the parent block"}

/// caption

///

![type-suggestion](./assets/images/type_suggestion_7.png){title="Infer from the parent block"}

/// caption
Fig 4: Infer from the parent block
///

The type constraint builder tries to infer the type from the attached input block first, then the parent block. 

![type-suggestion](./assets/images/type_suggestion_6.png){title="From the attached block, then the parent block"}

/// caption
Fig. 5: From the attached block, then the parent block
///
