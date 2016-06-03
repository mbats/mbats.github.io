---
layout:     post
title:      "Let me Sirius that for you"
subtitle:   "Properties view"
date:       2016-05-26 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-02.jpg"
---
It’s been a while since my last [Eclipse Sirius post](http://melb.enix.org/sirius/sirius-3-0/) but this year we [_Get Busy_](https://youtu.be/oPQ3o14ksaM?t=11) at Obeo with the preparation of the new Sirius release. It is a really important release for me as I am contributing _[For the very first time](https://youtu.be/zHW5RVvg2v4?t=68)_ as an [Eclipse commiter](https://projects.eclipse.org/content/melanie-bats-committer-extended-editing-framework-eef) ![:)](http://melb.enix.org/wp-includes/images/smilies/icon_smile.gif)

I am really proud to be part of the Eclipse community and excited to meet her again at EclipseCon France. _[I hope you’ll join us](https://youtu.be/yRhq-yO1KN8?t=107)_ to attend our talk [Sirius 4.0: Let me Sirius that for you!](https://www.eclipsecon.org/france2016/session/sirius-40-let-me-sirius-you)

You already know that Sirius allows you to create _[So powerful](https://youtu.be/Y7OCgi7rANc?t=63)_ <span style="font-weight: 300;">graphical designers. With minimal efforts you can create a great modeler with a ready-to-use graphical editor providing a model explorer, a palette, a toolbar and contextual menus dedicated to your own DSL.</span>

But when you create a dedicated designer after specifying the viewpoints, the mappings and the tools, the next step is most of the time to contribute dedicated properties views in order to ease data edition.

Thanks to the Eclipse modeling ecosystem, there are already several solutions to contribute form-based views to Eclipse applications: [EEF](https://eclipse.org/eef/), [EMF Forms](http://www.eclipse.org/ecp/emfforms/), [EMF Parsley](https://www.eclipse.org/emf-parsley/documentation.html).

All these solutions can work with Sirius based modelers through an extension point and it will remain so. But what we have seen is that for many people the gap in between the “Sirius way” and the “Other frameworks” way is large and they are often groping for the constructions they are used to in Sirius. At that point you feel like, _[This is the way you left me](https://youtu.be/vzoYgasvKdo)_… Very transversal things like colors or editing behavior are defined in a Viewpoint Specification Model and the users needs to refer to those things for their property views. A property views definition which is perceived as more complex than the graphical modeler defeats the whole approach.

At the end of last year, we decided to do something for you to improve the situation. You guys _[Get lucky](https://youtu.be/h5EofwRzit0)_!

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/Get_Lucky.jpg)

I am very pleased to announce that from here on out **Sirius provides** an **integrated way to define your properties views** in the same way as you are used to define the other parts of your designer: no need for code, it is dynamic and query based.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/properties-view-vsm.png)

With Sirius 4.0, you are able to specify exactly how your properties view should be represented. If you already know Sirius, it is fairly _[Easy](https://youtu.be/ST7btkkoaNU?t=33)_.

As you are used to do with other kind of representation in Sirius, you can specify mappings between graphical properties view elements and semantic elements.

Once you installed the right plugins, in the VSM (the configuration file which defines your modelers in Sirius) you can create a new kind of extension under which you can specify Pages, Groups and Widgets. A page represents a tab of your properties view and a group represents a section. Several widgets are available to represent you semantic elements: text, text area, checkbox, select… and it is very easy to add your own if needed.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/structure.png)

For each kind of widgets, you can define specific styles based on the semantic model. Exactly like it is already possible for diagrams, conditional styles can be applied based on evolving values of your semantic model.

It is also possible for each widget to define a specific behavior. You can specify the behaviour associated to: the text widget edition, the onclick event of an hyperlink/a table, a pushed button, etc. For example, to define the behavior of the text when a change occurs, you simply specify the behavior associated to the edition inside the _Begin_ element using all the usual [model operations](https://www.eclipse.org/sirius/doc/specifier/general/Model_Operations.html).

<a>![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/edition.png)</a>

One of the main advantage of Sirius is that the graphical representations are independent from the metamodel’s structure. The same principle was kept for developping the properties views feature. This means that you can choose **not** to respect the containment hierarchy of your model when you display it graphically. This is possible because Sirius is based on [queries](http://www.eclipse.org/sirius/doc/specifier/general/Writing_Queries.html).

For example, we can represent the same attribute with different widgets. Below, you can see that the _Location_ can be represented thanks to a _Select_ or a _Radio_ widget.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/queries1.png)

We just specify two different widgets in the properties view description, one for the _Select_ :

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/queries2.png)

And one for the _Radio_:

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/queries3.png)

In each case, the _Candidate Expression_ and _Value Expression_ are used to query the model and get the expected semantic elements.

One last thing, with the Sirius 4.0 version, when you create a modeler, by default you can get **for free** beautiful default **properties views** without defining anything special in your VSM.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/default.png)

How does it work? _[It’s a kind of magic…](https://youtu.be/0p_1QSUsbsM?t=11)_

We do the work for you by providing default rules based on the type of the elements defined in your metamodel. For example, if you have defined a string attribute in your metamodel, it will be automatically represented with a text widget, a boolean will be represented with a checkbox, etc.

If the default properties view does not fit what you need, no problem specify your own properties view as explained above.

There are plenty of other awesome features, such as context based properties views, dynamic mappings, validation, quick-fixes and more. If you want to learn more, join us at EclipseCon France:

*   on thursday afternoon june 7th, [Sirius workshop](https://www.eclipsecon.org/france2016/session/sirius-workshop-lets-create-graphical-modeling-editor-robot),
*   on wednesday afternoon june 8th, [Sirius 4.0 talk](https://www.eclipsecon.org/france2016/session/sirius-40-let-me-sirius-you),
*   all day long visit the [Obeo booth](https://www.eclipsecon.org/france2016/sponsor/obeo).

What you think is _[Give it to me baby!](https://youtu.be/AltMeuPkWRs?t=74)_ This feature will be delivered as _experimental_ with Sirius 4.0 which comes with Neon, and be available officially in Sirius 4.1 expected after Neon.1\. Even if it is tagged as experimental, it is ready to use. And do not be afraid, try it, we will take care of the migration for you as we usually do for other parts of Sirius, it will be completely transparent for you to upgrade from 4.0 to 4.1 when it becomes available.

![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/bart.png)

Come on and _[try it on your own](https://youtu.be/aA9mmz508Ro?t=58)_!
