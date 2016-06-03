---
layout:     post
title:      "I am your container"
subtitle:   "Darth Sirius"
date:       2015-04-30 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-01.jpg"
---
Continuing the [Sirius](http://www.eclipse.org/sirius/) blog [posts series](http://melb.enix.org/category/sirius/), today we will see a small tip: how to create artificial containers in your diagram?

One of the main advantage of Sirius is that the graphical representations are independent from the metamodel’s structure. This means that you can choose to not respect the containment hierarchy of your model when you display it graphically. This is possible thanks to Sirius being based on [queries](http://www.eclipse.org/sirius/doc/specifier/general/Writing_Queries.html).

In the following example, we define a metamodel of a family:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/Metamodel.png)

To begin with, we define a _Flat_ diagram, which displays all the members of the family at the same level:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/Flat_VSM.png)

In the _Person_ mapping, we use the _Semantic Candidates Expression_ to provide which semantic elements must be represented. These expressions returning model elements are called [queries](http://www.eclipse.org/sirius/doc/specifier/general/Writing_Queries.html). To write these queries, there are different languages provided by default in Sirius: specialized interpreters (`var`, `feature`, `service`), Acceleo, raw OCL or Java. Here, we use the _feature_ interpreter to get for a family all the persons referenced by the `members` reference. You can easily identify _interpreted expressions_ by their yellow background in the Properties tab of an element.

We create a first diagram which represents the flattened Skywalker family:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/Flat.png)

The next step is to add a level to model the _Family_ as a container. We create a new _Family_ diagram which contains a _Family_ container mapping and a _Person_ mapping as sub nodes:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/Family_VSM.png)

The _Family_ diagram is created and all the members are represented inside the Skywalker container.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/Family.png)

Here we represent graphically the containment reference `members`. But what to do if we want to create an _artificial_ container which does not exist in the metamodel as a containment reference?

Let’s see! Now imagine that we want to add a level to represent [The Force](http://en.wikipedia.org/wiki/The_Force_(Star_Wars)) and if the person is related to the dark side or the light side. To do this we create a new _ForceSide_ diagram:  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/ForceSide_VSM.png)

We add a new container to represent the _DarkSide_ of the force :  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/DarkSide_VSM.png)

The dark side must be represented once for each family, the semantic candidate returns _var:self_ which means the current family. As it should contain persons, it is defined as a _FreeForm_ container.

We need to represent, in the Dark Side container, the persons that are from the dark side of the force. So we define a new sub node _Person_ with the Semantic expression set to: `[self.members->select(p|p.oclAsType(Person).dark)/]`  
This query returns all the members of a family and selects only the _Person_ which has the attribute `dark` set to true.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/Sith_VSM.png)

Then we reuse the _Person_ mapping to represent the person in its force side container.

Finally, we do the same for the light side of the force and we create a `LightSide` container and the `Person` mapping to represent members of the family in this new container who are influenced by the light side: `[not self.members->select(p|p.oclAsType(Person).dark)/]`  
A new `ForceSide` diagram is created in the Skywalker family and we discover that only Darth Vader is from the dark side of the force and that his children are driven by the light side of the force.  
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/artificial-container/blog/images/ForceSide.png)

Thanks to the queries in Sirius, it is easy to create artificial containers which are not related to containment referencers in the metamodel.

_“May the **Sirius** Force be with you”_ ![;)](http://melb.enix.org/wp-includes/images/smilies/icon_wink.gif)

The sample code from this example is available on github: [https://github.com/mbats/sirius-blog/tree/master/artificial-container](https://github.com/mbats/sirius-blog/tree/master/artificial-container)