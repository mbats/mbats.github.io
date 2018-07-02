---
layout:     post
title:      "Sirius 6"
subtitle:   "The Future of modeling tools"
date:       2018-07-02 10:00:00
author:     "Mélanie Bats"
header-img: "img/up-to-the-cloud/post-bg.jpg"
tags: [planet]
---
[Eclipse Sirius](https://www.eclipse.org/sirius/) is a framework to easily and quickly create a graphical modeling workbench dedicated to your domain specific language.

This year at [Obeo](https://www.obeo.fr/en), we started working on two aspects: **prepare the future of Sirius** & provide **new features for the upcoming 6.0** release which is part of the Photon release train.

**Ready for Photon? Sirius 6.0 is there for you!**

We have added several new features:
* **Support for background color on diagrams**: it is now possible to dynamically compute the color of the diagram according to the state of the model. This is a small feature, but it continues to expand the visual customization capabilities available to specifiers.
![Background color on diagrams](/img/futur-of-modeling-tools/diagram_background.png)

* **New “magic” edge creation tool**: All diagrams will now benefit for free from a new smart edge creation tool. Thanks to this end users no longer have to chase for the appropriate tool in the palette (which can contain many entries): just click on the source and target of the edge to create and Sirius will automatically detect which tools can be applied to them. If there is only one, the edge is created immediately. If several tools are possible as is the case of the animation, a menu opens to choose among the candidate tools.
![New “magic” edge creation tool](/img/futur-of-modeling-tools/runtime_sirius_demo2.gif)

* **Quick navigation to service method implementation**: Real-world modelers often need to call into Java code to perform complex operations on models or call into Sirius and Eclipse APIs. This is very straightforward to do in Sirius with the notion of Java services that can be transparently invoked from AQL expressions. It is now possible to navigate from the expressions in the Sirius specification which invoke a service method directly into the corresponding Java code with a single keystroke.
![Quick navigation to service method implementation](/img/futur-of-modeling-tools/runtime_sirius_demo.gif)

* **Integration with ELK for improved diagram layouts**: Sirius has always proposed an automatic layout algorithm. Specifiers can now leverage the high-quality layout algorithms provided by the Eclipse ELK project. You can choose any of the algorithms proposed by ELK and tweak all their configuration parameters in the Sirius specification. The end users will transparently get a nicer layout when using the existing “Arrange All” action. This is experimental in Sirius 6.0. Give us feedback on which aspects to focus on for the future.
![Integration with ELK for improved diagram layouts](/img/futur-of-modeling-tools/runtime_sirius_sm.png)
![Override ELK options](/img/futur-of-modeling-tools/override_options.png)

**What’s next**?

We are working on what would be the future of modeling tools. We already gathered 
some feedback from the community. You expect that modeling in the future would be: **fast, simple, easy, beautiful, cloud & collaborative**.

We believe that the concept of IDE is evolving. In the future, we will have more accessible tools and better tool integration. In the end, we think that tools should become IDE agnostic.  We will have more and more tools dedicated to specific domains. These tools would be available more broadly, for various kind of users on any kind of platforms. We need frameworks to ease the creation of such specific tools dedicated to one usage. That’s why we believe in frameworks such as Sirius.

Sirius is a really nice framework to create dedicated desktop workbenches based today on the Eclipse platform. Our purpose is to bring the spirit of Sirius to the cloud: easily develop modeling workbenches but rendered in a browser and integrable in any web application.

So where are we today? We are going step by step and work on different aspects.

1. **Introduce web technologies in existing Eclipse views**: Our first step is to introduce web technologies in existing Eclipse views. This approach is used to provide a brand new feature in Sirius 6.0 called Workflow which allows specifiers to guide users through the usage of their workbench. On the left of the following screenshot, we see a Sirius configuration file which defines a workflow with different actions using this new DSL. To the end-user, these are rendered as web elements inside the Eclipse view. Note that this new feature is still experimental in 6.0, and will be improved for version 6.1 this fall.
![Web components in Eclipse view](/img/futur-of-modeling-tools/webcomponents_sm.png)
1. **Make Sirius independent from Eclipse platform**: The idea is to make the Sirius code base more modular, isolating the core business concerns from the current Eclipse-based technology stack: the Eclipse UI, GMF, the workspace, and even the Eclipse Runtime itself. We will work on this progressively over several versions, making sure Sirius always keeps working even in the classical Eclipse-based context. The end goal is to get a set of core components that can be reused both in Eclipse and, more to the point, inside a web server exposing its services to any web client through a well-defined protocol.
1. **[Render Sirius diagrams in a browser](https://www.youtube.com/Ua3-93O3TRs)**: Based on a classical Sirius configuration, we can render in a browser the graphical elements of a diagram. As usual, the specifier can work on the look and feel of his modeler iteratively. This prototype is based on Sprotty. Sprotty is a new project proposed to the Eclipse Foundation by TypeFox. It is a small, lightweight, open source & well architectured JavaScript graphical library providing rendering in SVG & well integrated with Eclipse ELK which provides auto-layout.
1. **Sirius integrated with Cloud IDEs**: Sirius in a near future will be IDE-agnostic. Then you will be able to integrate Sirius based workbenches in any web application or any IDE. Have a look at the prototypes we already have of Sirius integrated in Eclipse Theia and of Sirius integrated in Eclipse Che.
![Sirius integrated with Cloud IDEs](/img/futur-of-modeling-tools/sirius_components_sm.png)
To sum up, we will keep working on the existing Sirius project and we will reintegrate the new web-related features and components. This summer we will continue our work on the modularization of the architecture. And for the 6.1 this fall, we will contribute a first version of web based diagrams based on the Graphical Server Protocol. 
![Sirius timeline](/img/futur-of-modeling-tools/diagram_workflow.png)

At Obeo, we’re taking a community-first approach to influence the development of the next generation of modeling tools. Please tell us what you want! We have lots of ideas for the future of Sirius. But what we need is to know what YOU need. So please Speak Up!

<iframe width="560" height="315" src="https://www.youtube.com/embed/OQRFUyBt1r4" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
