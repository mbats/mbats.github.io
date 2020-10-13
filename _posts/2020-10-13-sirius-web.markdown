---
layout: post
title: "T-8:00 1st stage Sirius Web loading begins"
subtitle: "SIRIUS-II Mission: Open sourcing Sirius Web"
date: 2020-10-13 10:00:00
author: "Mélanie Bats"
header-img: "img/siriusiimission/post-bg.jpg"
tags: [planet]
---

Source code is flowing into the first stage of the Obeo rocket. Our goal is to bring the spirit of Sirius into a new technological space : Sirius Web is the Cloud-based evolution of Sirius, 100% Open Source.

![](/img/sirius-web/SiriusWebTimeline.png)

The Sirius Web engine combines the open source components EMF-JSON & Sirius Components. These components will be available under the Sirius project : [http://eclipse.org/sirius](http://eclipse.org/sirius), with the source code on Github :

- **EMF-JSON** is a small library to serialize EMF models to JSON,
- The **Sirius Components** repository provides backend and frontend components
- The **Sirius Web** repository combines the open source Sirius components to provide a graphical modeler sample application.

![](/img/sirius-web/SiriusWebArchitecture.png)

## How do you create a cloud-ready modeler based on Sirius Web?

1. Define your metamodel thanks to EMF.
2. Provide a Sirius configuration to specify the mapping between the different concepts of your DSL and how they should be represented graphically.
3. Register the metamodel & the Sirius specification in the Sirius Web application.
4. Build and launch the application!

![](/img/sirius-web/SiriusWebServer.png)

As a result, you get a graphical modeler dedicated to your DSL rendered in your browser.

<iframe width="560" height="315" src="https://www.youtube.com/embed/IXXxOCbEjE4" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

To get more details about Sirius Web and how to run it for your own DSL, attend Obeo’s rocket liftoff.
Launch remains on schedule for [October 21 at 2:00 p.m CET](https://www.eclipsecon.org/2020/sessions/sirius-web-100-open-source-cloud-modeling-platform).
