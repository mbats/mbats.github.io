---
layout:     post
title:      "Super powered API"
subtitle:   "Sirius 4.0 Gotta Catch ‘Em All"
date:       2016-06-20 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-02.jpg"
---
You already discovered with the [previous posts](http://melb.enix.org/sirius/sirius-4-0-stability-and-performance) that Sirius is more and more powerful. Sirius 4.0 offers more and more possibilities to our advanced users thanks to super powered APIs. 

**API to control the tab-bar** 
[![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/butterfree.png)](http://orig07.deviantart.net/747b/f/2014/068/a/7/butterfree_by_weaponix-d79lwes.png) 
The top area of all Sirius diagram editors is filled with the tab-bar, which provides access to many operations on diagrams and their elements. From now on, Sirius provides an API to get complete control of how the tab-bar is filled: which elements to put (Sirius standard ones or custom ones) and in which order. 
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/tabbar.png) 

**Better integration with EMF Edit** 
[![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/exeggcute.png)](http://orig00.deviantart.net/89b8/f/2014/308/2/0/exeggcute_by_weaponix-d85bhkz.png) 
For the specifier, Sirius 4.0 comes with a better integration with EMF Edit. While it is only the beginning, Sirius is now contributing the EditingDomainServices service class, which can be referenced from any VSM. This class provides a large set of methods giving access to many useful features of the EMF Edit framework. It provides general editing domain related services and contributes all types of Item Providers, in a way that is directly accessible as service invocations from interpreted expressions. It also offers item property related services. A series of service methods can be used to invoke the standard EMF Commands available from and ItemProviderAdapter’s various createXXXCommand() methods. Note that contrary to the createXXXCommand() methods which simply returns a Command instance, the service methods exposed in this class will directly execute the command on the editing domains CommandStack. 
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/emfedit.png) 
To [catch all](https://en.wikipedia.org/wiki/Gotta_catch_%27em_all) the new features coming with Sirius 4.0 have a look at the slides of [our talk](https://www.eclipsecon.org/france2016/session/sirius-40-let-me-sirius-you) at EclipseCon France! Another chance for you to join the Sirius community, [SiriusCon](http://www.siriuscon.org/) will occur in Paris the 15th November 2016\. Be sure to save the date!