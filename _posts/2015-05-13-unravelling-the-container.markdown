---
layout:     post
title:      "Unravelling the container "
subtitle:   "within the container within the container"
date:       2015-05-13 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-01.jpg"
---
Last time in the [Sirius](http://www.eclipse.org/sirius/) blog [post series](http://melb.enix.org/category/sirius/), you learned how to create an [artificial container](http://melb.enix.org/sirius/artificial-container/), today we will see how to create an infinite hierarchy of containers.

As an example we will represent the different dream levels featured in [Inception](http://en.wikipedia.org/wiki/Inception) :

[![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception_poster.jpg)](http://minimalmovieposters.tumblr.com/post/32154330691/inception-by-ojasvi-mohanty)

We need to model dream levels and that levels can refer to other sub levels :  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/metamodel.png)

We develop a first `Flat` representation to show all the levels at the same stage :  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/flat_vsm.png)

A `Flat` diagram is created and a `Level` container is defined to represent all the levels defined in the model :  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/flat.png)

Thanks to this representation we see all the different dreams but it is not possible to understand how they are interlinked.

Next step we create a `SubLevel` diagram to represent the first three dream levels :  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/sublevel_vsm.png)  
A first container `Level` represents the reality, then we represent the second dream level thanks to the `SubLevel` container and finally the third level with another container named `SubSubLevel`.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/new_container_menu.png)

For each container we retrieve the child level thanks to the `levels` feature defined in the metamodel. For each level container we define a new style.

The following `SubLevel` diagram results:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/sublevel.png)

Defining for each level a new mapping and a new style is really painful and it determines the number of levels you can create. Fortunately, Sirius can help us to define an infinite hierarchy of elements.

## Reuse mappings

We create a new `Inception` diagram as we did before, we define again a `Level` container to represent the initial level and then a `SubLevel` mapping models the second level.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception_vsm_level.png)  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception_vsm_sublevel.png)

At this point we are able to represent only the first two levels. To get an infinite hierarchy of levels, we need to set in the `Import` tab, the `Reused Container Mappings` field and select the `SubLevel` mapping. This means that the _SubLevel_ mapping could define as descendant other _SubLevel_ mappings. Here we reuse a mapping defined elsewhere in the VSM using the [Reused Mappings property](http://www.eclipse.org/sirius/doc/specifier/diagrams/Diagrams.html#containers) in the Import category. The effect at runtime is the same as if you had created an equivalent mapping inside the parent mapping.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception_vsm_sublevel_import.png)

We create a new _Inception_ diagram and…It’s working like a dream! We see all the levels hierarchy.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception.png)

Pay attention, as this method uses recursion, if you set the semantic candidates expression to _eAllContents_ a stack overflow exception will occur.

Last point, using this method we need to define the style for the first level and then we set the same style values to the sublevel mapping in order that all the levels appears with the same look.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception_vsm_styles.png)

With Sirius you can define the level style just once.

## Import mappings

A last `Inception2` diagram is defined, with a `Level2` mapping which is an exact copy of the previous `Level` mapping. We define also a style for this mapping.  
Then instead of creating a _New Diagram Element_ as we did in the previous diagram definition, this time we create a _New Import Element_.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/new_container_import_menu.png)

The _Semantic Candidates Expression_ is set to `feature:levels`  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception2_vsm_sublevel.png)

And in the _Import_ tab, we set the `Imported Mapping` to Level2\. This means that this new mapping reuses the style defined by the imported mapping.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception2_vsm_sublevel_import.png)  
The [mapping imports](http://www.eclipse.org/sirius/doc/specifier/diagrams/Diagrams.html#mapping_imports) are used to specialize an already defined mapping. In our example we override the _Semantic Candidates Expression_.  
To get an infinite hierarchy of levels, we set again the `Reused Container Mapping` field to SubLevel2.

Then in this diagram definition the level style is defined just once:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception2_vsm_style.png)

If we create an `Inception2` diagram we obtain exactly the same result as before :  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/reimport/blog/images/inception2.png)

With Sirius, make your dreaming designer come true!

The sample code from this example is available on github: [https://github.com/mbats/sirius-blog/tree/master/reimport](https://github.com/mbats/sirius-blog/tree/master/reimport)