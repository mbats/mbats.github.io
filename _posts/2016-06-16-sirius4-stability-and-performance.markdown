---
layout:     post
title:      "Stability and Performance"
subtitle:   "Sirius 4.0 Gotta Catch ‘Em All"
date:       2016-06-16 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-02.jpg"
---
Release after release, [feature](http://melb.enix.org/sirius/sirius-4-0-improve-user-experience) after feature, the goal of the Sirius team is to provide a stable and efficient framework to our users. So as usual we worked with this goal in mind for the Sirius 4.0 release. 

**Edges labels stability**
[![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/tauros.png)](http://orig08.deviantart.net/504f/f/2014/342/0/e/tauros_by_weaponix-d896r5q.png) 
We worked on several improvements to the diagram editor to offer a better experience to the end user. For example, we improved the edge label stability. With Sirius 4.0 when you move an edge the label stays close to the edge. 
![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/edgeslabelstability.gif) 
**Improve performance on session unload** 
The Sirius team works as well on improving performance. A significant improvement has been brought in the 4.0 release on session unload. Now Sirius will no longer spend time calling unload on the resources that will no longer be used. Thanks to this, the unload operation is now almost immediate. Note, that it is possible to customize this behavior if needed by specific resources implementations or usage contexts. 
[![](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/rapidash.png)](http://orig14.deviantart.net/f8b2/f/2014/250/1/8/rapidash_by_weaponix-d7ycanl.png) 
<span style="font-weight: 300;">To [catch all](https://en.wikipedia.org/wiki/Gotta_catch_%27em_all) the new features coming with Sirius 4.0 have a look at the slides of</span> [our talk](https://www.eclipsecon.org/france2016/session/sirius-40-let-me-sirius-you) <span style="font-weight: 300;">at EclipseCon France! Another chance for you to join the Sirius community,</span> [SiriusCon](http://www.siriuscon.org/) <span style="font-weight: 300;">will occur in Paris the 15th November 2016. Be sure to save the date!</span>