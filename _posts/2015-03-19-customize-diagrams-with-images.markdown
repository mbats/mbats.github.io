---
layout:     post
title:      "Customize diagrams with images"
subtitle:   
date:       2015-03-19 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-01.jpg"
---

Continuing from the example of our [previous blog post](http://melb.enix.org/sirius/the-tree-layout-secret) on House of Cards, we’ll see today how one can customize the elements of diagrams by using pictures.

## Per-diagram instance customization

In a Sirius based editor, the style of each diagram element can be customized. This customization can be applied from:

*   the tool bar:

![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/toolbar.png?raw=true)

*   the `Appearance` tab of the property view:

![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/appearance.png?raw=true)

*   the `Diagram` menu:

![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/diagram.png?raw=true)

*   the contextual menu `Format`:

![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/format.png?raw=true) The elements you can customize are:

*   container: background color, background style, border size, foreground color, label alignment, label size, label format and workspace image.
*   node: border size, color, label alignment, format, position, size and workspace image.
*   edge: the folding style, the color, the label alignment, format, position and size, the line and routing style, the size and the target and source arrow.

If we set a workspace image on the _Influence_ diagram resulting from the [tree layout blog post](http://melb.enix.org/sirius/the-tree-layout-secret), we are able to see Frank Underwood’s face instead of a simple white square. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/set_image_on_existing_diag.png?raw=true) These customizations can be reset using:

*   the `Reset style customization` button available in the `Appearance` tab of the property view :

![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/appearance_reset.png?raw=true)

*   in the diagram editor tool bar :

![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/toolbar_reset.png?raw=true) Thanks to this feature each user can customize existing diagrams in any Sirius based modeler. The problem with this solution is that if you create another diagram, the default style will be applied, and we would no longer see Frank’s beautiful face. This method is only useful to customize a specific instance of a diagram.

## Using workspace image style

If instead of having customization specific to a given instance, we would like all diagrams of a certain type, what we need to do is to provide the image during the diagram specification phase. In order to get the image on every new diagram, we need to provide it at the diagram specification phase. To do so, after reopening the `houseofcards.odesign`, we need to update the _Influence_ diagram description to use a workspace image in a conditional style to represent Frank. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/conditional_styles_specification.png?raw=true) From now on, everytime an _Influence_ diagram is created, Frank’s and Linda’s faces will automatically be associated to the relevant diagram elements. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/conditional_styles.png?raw=true) What is problematic with this solution is that we need to create a conditional style for each character. As there are around 50 different characters in the House of Cards series, it is not a very practical solution.

## Specify style custom images

Fortunately, Sirius provides another way to achieve that. We want to provide all the images in a specific folder and have Sirius select the right one according to the picture’s name. This can easily be done by using the `style customizations`. We modify our mapping to specify a workspace image style. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_mapping.png?raw=true) We provide a new style customization: ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_specification.png?raw=true) And a new property customization by expression: ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_property_specification.png?raw=true) All the pictures are stored in an `images` folder. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_design_images.png?raw=true) Then we specify that the style to customize is the workspace image previously defined. This style customization must be applied on `PersonWorkspaceImage` and we want to customize the `workspacePath` property: ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_property_specification2.png?raw=true) To retrieve the value of the `workspacePath`, we call a Java service `getImage` which returns the image path from the person name: ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_java.png?raw=true) Finally, when we reopen our example, we get a shinier diagram this time with everybody associated to his picture. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_property.png?raw=true) And now if I update the name of a character, I get automatically the associated picture. John Doe is represented by the default image and we see Zoe’s lovely face. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/style_custo_update_name.png?raw=true) With the next Sirius 3.0 version, if you use images with a transparent background, the edges will follow the image. ![](https://github.com/mbats/sirius-blog/blob/master/custo-diag/blog/images/Sirius_3_0_Edges_And_Transparency.png?raw=true) The sample code from this example is available on github: [https://github.com/mbats/sirius-blog/tree/master/custo-diag](https://github.com/mbats/sirius-blog/tree/master/custo-diag "https://github.com/mbats/sirius-blog/tree/master/custo-diag")