---
layout:     post
title:      "Improve user experience"
subtitle:   "Sirius 4.0 Gotta Catch ‘Em All"
date:       2016-06-14 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-02.jpg"
---
To continue with the Sirius 4.0 new features [serie](http://melb.enix.org/sirius/sirius-4-0-border-song/), today we will show how we improved the user experience.

**Bi-directional link with editor**

[![doduo_by_weaponix-d8380qe.png](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/doduo.png =144x)](http://orig03.deviantart.net/ca6f/f/2014/290/3/7/doduo_by_weaponix-d8380qe.png)

When exploring a complex model, users frequently need to switch from the tree representation (provided by the Model Explorer) to the current diagram and vice-versa. Before Sirius 3.1, the “link with editor” option was uni-directional: selecting a model element in the Model Browser was selecting the same element in the diagram, but not the opposite. Now, this option is bi-directional: selecting a diagram element automatically selects the corresponding model element in the Model browser.
![linktoeditor.gif](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/linktoeditor.gif)

**Selection after tool execution**

[![exeggutor_by_weaponix-d85fbsd.png](https://raw.githubusercontent.com/mbats/sirius-blog/master/sirius4/blog/images/exeggutor.png =144x)](http://orig03.deviantart.net/3ee8/f/2014/309/8/9/exeggutor_by_weaponix-d85fbsd.png)

For users who need to rapidly create new models and efficient representations, reducing the number of clicks is very important to improve their productivity. With Sirius 3.1, we have added the possibility to specify which elements to automatically select after a tool execution. For each kind of tool (creation, edition, navigation, etc), we have added two new options “Element To Select” and “Inverse Selection Order” that can be used to specify which model elements to select after the execution of the tool.
![post-execution_options.png](https://lh4.googleusercontent.com/mxHFA_WNbyw6384Q8ARWnM2i8a3QCvr1_ZPw5wuufD7oi8RBoSf46H4r5LqH2NX5awJzmRcDjws2LkHSOKXl0hynqlzZ1HYOgZKIJ3-X8Z30pJ-IwF_Awq35-fOvyzmRIwfvw1Fr =283x)
To catch all the new features coming with Sirius 4.0 have a look at the slides of [our talk](https://www.eclipsecon.org/france2016/session/sirius-40-let-me-sirius-you) at EclipseCon France! Another chance for you to join the Sirius community, [SiriusCon](http://www.siriuscon.org/) will occur in Paris the 15th November 2016. Be sure to save the date!