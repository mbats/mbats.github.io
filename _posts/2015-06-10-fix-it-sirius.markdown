---
layout:     post
title:      "Fix it Sirius!"
subtitle:   
date:       2015-06-10 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-01.jpg"
---
This week the [Sirius](http://www.eclipse.org/sirius/) blog [post series](http://melb.enix.org/category/sirius/) presents «How to integrate validation rules on a diagram ?».

EMF provides a powerful validation system which helps you detect errors in your model. But sometimes you would like to add more rules not already implemented in your metamodel. Sirius is there again!

Imagine that we would like to represent the well known Arcade game from the [Wreck it Ralph!](http://en.wikipedia.org/w/index.php?title=Wreck-It_Ralph) movie.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/Wreckitralphposter.jpeg)

We define a metamodel to represent the `Building` present in the game.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/metamodel.png)

We also define an `isFixed` attribute that indicates whether the building is broken or not and so if it needs to be fixed.

## Semantic validation

Then we create a new Sirius specification project and we define a viewpoint with a new diagram named `SemanticValidation`. A `Building` mapping is added and provides two different styles according to whether the building is broken or not.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/semanticvalidation_vsm.png)

We create a model example defining a `Game` element and a `Building`, we activate our new viewpoint and create a new _SemanticValidation_ diagram.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/semanticvalidation.png)

We create also a _Wreck it_ tool which can be applied on a Building and set the `isFixed` attribute to `false`. After applying the tool on the building the diagram looks as below:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/semanticvalidation_wreck.png)

Next a rule is defined to detect when the `isFixed` attribute is set to `false`. We improve our diagram specification by adding a new [Validation rule](http://www.eclipse.org/sirius/doc/specifier/diagrams/Diagrams.html#validation). To do so on the diagram specification element, select `New Validation > Validation` and create a `Semantic Validation Rule`.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/semanticvalidationrule_vsm.png)

Then, we set :

*   the `Level`: severity of issues reported when the validation rule is broken. It could be `Information`, `Warning` or `Error`.
*   the `target class`: type of semantic element checked by the rule.
*   the `Message`: message shown to the user in the _Problems_ view when the validation failed.

An `Audit` element must be also defined to provide the expression that must be checked to validate the rule. When the expression evaluates to true, no validation issues are reported. Otherwise, issues will be listed in the _Problems_ view. It is possible to define several audits for one rule, in this case the rule is considered as violated if at least one audit applies.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/audit.png)

The user can call the validation thanks to a right click on the diagram background and by selecting the _Validate diagram_ menu:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/validate_diagram.png)

If we activate the validation on our wrecked building, we get one error:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/semanticvalidation_error.png)

On the diagram, the validation issue is also visible thanks to an error decorator added on the figure:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/error_decorator.png)

## View validation

Another possibility is to define validation rules based on graphical elements instead of the semantic ones.  
We create another representation named _ViewValidation_ which provides a view validation rule:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/viewvalidationrule_vsm.png)

In this case, the validation rule will be applied on a mapping.

This time an error will be thrown when the border color RGB red component of the building will be different than 239.  
We define also a quick fix which also modified the semantic model to fix the building again.

## Quick fix

Eclipse users love their IDE because it is very often capable of proposing a _Quick fix_ functionality for typical problems. Sirius allows to easily implement such a Quick fix feature, let’s call it _“Felix quick fix it”_:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/Fix-It-Felix.jpg)

On the validation rule element, we define the `Fix`.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/fix_vsm.png)

We set the fix message and define how the fix will update the model. Finally if we launch the quick fix on our example, it just changes the value of the `isFixed` attribute to `true`.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/quickfix1.png)  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/quickfix2.png)

Thanks to Sirius and Felix our building is all fixed.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/validation/blog/images/semanticvalidation.png)

You can wreck it again… thanks Ralph…

The sample code from this example is available on github: [https://github.com/mbats/sirius-blog/tree/master/validation](https://github.com/mbats/sirius-blog/tree/master/validation)