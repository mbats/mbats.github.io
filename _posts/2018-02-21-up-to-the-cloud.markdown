---
layout:     post
title:      "Modeling tools go up to the cloud"
subtitle:   "... and beyond"
date:       2018-02-22 10:00:00
author:     "Mélanie Bats"
header-img: "img/up-to-the-cloud/post-bg.jpg"
tags: [planet]
---

TLDR; at [Obeo](https://www.obeo.fr/en), we have done the first steps to **bring Sirius to the web**. Today we are ready to work with you to bring **your own modeling tool up to the cloud**.

If you are curious about details, this is the longer story…

As you know, at Obeo, we have been working on modeling tools for a long time now, and we therefore have a lot of experience developing graphical tools. Obeo is a key player in the Modeling ecosystem: we are involved in open source through numerous Eclipse projects: [Sirius](https://www.eclipse.org/sirius/), [Acceleo](https://www.eclipse.org/acceleo/), EMF/GMF, [EcoreTools](https://www.eclipse.org/ecoretools/), [EMF Compare](https://www.eclipse.org/emf/compare/)...
One of our great success is Sirius: a framework to easily and quickly create a modeling workbench dedicated to your domain.

Today, Sirius relies on the Eclipse platform, consequently the graphical modelers based on it are desktop applications.

You know that **Desktop** vs **Web** applications are in war since time immemorial...  

In the past, we already won some battles, by mixing both approaches, switching from one to another. 
For instance, our Enterprise Architecture solution [Obeo SmartEA](https://www.obeosmartea.com/en/solution), provides :
* light client experience to explore a model,
![Explore model with light client](https://www.obeosmartea.com/images/my_gallery/10-details-page.png)
* and a rich application to edit it.
![Edit model with rich application](https://www.obeosmartea.com/images/my_gallery/05-graphical-modeling-workbench.png)

Since December, you already know that we are working to reconcile the two worlds... For Sirius 6, we are developing a new solution to **use Sirius definition with HTML Renderer within Eclipse workbenches**. We will use an hybrid model to be able to get the best of both worlds and make them coexist in the same rich application. In collaboration with Thales, we are prototyping what would be a [Capella](http://www.polarsys.org/capella/) graphical modeler using the dynamic visualisation capabilities offered by [Sprotty](https://github.com/theia-ide/sprotty) and [Eclipse Layout Kernel](https://www.eclipse.org/elk/). I really appreciate that the [TypeFox](https://typefox.io/) guys lent us a hand about that, this was truly in the open source spirit! 

![HTML renderer within Sirius workbenches](/img/dear-santa/HTMLRendererInSirius.png)

I am really happy to announce that now we are going one step further: we are making Sirius evolve to **bring modeling tools up to the cloud**.

![Up](http://static.alfabetajuega.com/abj_public_files/multimedia/imagenes/201501/95918.alfabetajuega-up-10012015.jpg)

Modeling tools based on Sirius today look like this. You have a graphical editor with a palette to manage elements.
![Modeling tool today](/img/up-to-the-cloud/Today.png)

Modeling tools based on Sirius tomorrow could look like this. You still have a graphical editor with a palette to manage elements.
![Modeling tool tomorrow](/img/up-to-the-cloud/Tomorrow.png)

The main difference is that tomorrow Sirius applications will be based on web technologies, and therefore the graphical modelers will be cloud applications. With a cloud application :
* you **no** longer **need to install** it, it simply do not require any installation process,
* it does not occupy extra space on your hard drive,
* your graphical workbench is **easy to access** from any browser and you can use it from any device,
* it adapts to the workload increase.

There is still a long way to go.
![Path to go](/img/up-to-the-cloud/Architecture.png)

As said before, today our modeling tools are based on Eclipse RCP technologies.
We are working on a new architecture to make this work in a client/server world. 
Sirius will be split in different pieces providing services to clients rendering the modeling tool in the browser.

To bring those technologies further to the web, from day 1 we were convinced that we needed a standard communication protocol.
A few months ago, an impressive community effort was started around the Language Server Protocol to ease the integration of languages to textual editors. 
We found that inspiring and that's why we decided to start working on a [Graphical Server Protocol](https://github.com/ObeoNetwork/GraphicalServerProtocol).
This initiative defines the protocol between an editor or an IDE and a graphical server that provides graphical features like tools, mappings, layout, layers…
We based our work on what was done by Typefox in Sprotty.

I am glad to reveal our first prototypes of Sirius exposing its services through the Graphical Server Protocol to render diagrams specified in a browser.
Today we can take any existing graphical workbench specified with Sirius and render it in a browser. Not only we render the graphical elements but also we interpret at runtime the creation tools available in the palette according to the one defined in the Sirius specification. And as we can see on the following video, it is possible to create new model elements thanks to those tools from the palette.
<iframe width="560" height="315" src="https://www.youtube.com/embed/cOxQtBwKhow" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

In the next video, just by updating the Sirius specification as usual, you can see in the browser how the elements are rendered and you can work on the look and feel of your modeler iteratively.
Here at the beginning all the edges and labels are black. One can update the Sirius specification to set the men labels and edges in blue. Immediately when the configuration is saved you see that the colors changed in the browser.
<iframe width="560" height="315" src="https://www.youtube.com/embed/S1cyefHKOjU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

A diagram can provide different layers. This demo shows the capability to enable/disable layers.
It will filter accordingly the graphical elements visible in the diagram and the tools available in the palette. 
You see that the layout is automatically recalculated every time a layer is enabled to provide a smart layout for the diagram at all times.
<iframe width="560" height="315" src="https://www.youtube.com/embed/S1cyefHKOjU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

I believe that both desktop and web applications will continue to coexist for a long time.
While both desktop and web applications have their pros and cons, what is important is that the application fits users needs. Users don’t care whether your app is native or web based as long as it does the job properly.
We do not give up one world for another, we are making what is needed to get the best of the two worlds.

That's why we are really excited by the fact that Eclipse Che decided to replace its GWT IDE by a new one relying on modern technologies: [Theia](https://github.com/theia-ide/theia). Pursuing the same line as Eclipse RCP, Theia is an open framework that allows users to compose their own applications. I believe that this extensibility model should foster the emergence of a new ecosystem.Thanks to the extensibility offered by Theia, we can envision in the future the development of modeling tools for both desktop and web applications equally and even going further by integrating such tools to cloud frameworks such as Che.
![Mockup of Sirius based modeler integrated in Che](/img/up-to-the-cloud/SiriusInChe.png)

One of the expectation of the modeling community is to be able to simplify deployment, that's one of our initial goal by going to cloud based applications.

As you saw in our videos, we are making Sirius evolve to bring modeling tools to the cloud.

We need you to go beyond.

As open source is in our DNA, most of these changes will be contributed to Sirius. The actual Sirius project will evolve to a client/server architecture.
Let's work together to bring your tooling to this new platform !

We would also like to invite all of you to participate to the Graphical Server Protocol initiative to make this an open collaboration providing a common protocol for graphical editors.

Finally remember that we are available to work with other organizations to bring modeling tools to the Web, including integration with web & cloud tooling such as Theia & Che.

Contact us, join us, support us!

> We're gonna get it, get it together
> I know, we're gonna get it, get it together and flow
> We're gonna get it, get it together and go
> Up, and up, and up

[Coldplay up & up](https://youtu.be/BPNTC7uZYrI)