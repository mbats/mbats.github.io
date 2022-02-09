---
layout: post
title: "Happy New 2022.01.0!"
subtitle: "What's new in Sirius Web"
date: 2022-02-04 10:00:00
author: "Mélanie Bats"
header-img: "img/post-bg-04.jpg"
tags: [planet]
---

I know... I am late for an happy new year but I am not for an Happy New [2022.01.0](https://docs.obeostudio.com/#_version_2022_01_0)!
I'm in a dancing mood while I'm writing this... (and poor you) an idea comes to my mind: _"Why not associating a song to each new features?"_
It could be _funny_ and you'll result with a (terrible) soundtrack to play with this new version.
Follow me for a _musical_ ride through the new Sirius Web and OCP features!

**Calendar versioning**

<figure>
<blockquote cite="https://youtu.be/EIbuf0iZKq8">
January, February, March, April, May<br/>
June, July<br/>
January, February, March, April, May<br/>
June, July
</blockquote>
<figcaption>—Boney M., <cite><a href="https://youtu.be/EIbuf0iZKq8">Calendar song</a></cite></figcaption>
</figure>
For two years now, we have been working hard on [Sirius Web in the open](http://melb.enix.org/2020/10/13/sirius-web/). Since the last 2021.12.0 version, Sirius Web released its first stable version. Since that point, we will take care not to break (too much) APIs for our [Sirius Components](https://github.com/eclipse-sirius/sirius-components) consumers. We decided to [switch from semantic versioning to calendar versioning](https://github.com/eclipse-sirius/sirius-components/blob/master/doc/adrs/034_switch_from_semver_to_calver.adoc) to reflect the maturity of the project.
We will keep our development cycle with six weeks of work and two weeks for various minor improvements for each release.
Once a stable release "YEAR.MONTH.0" is done, we will start working on the next one "YEAR.MONTH+2.0". During the preparation of the next release, we will improve the current branch to prepare for that release. As a result, we will have multiple intermediate releases with a YEAR.MONTH.1, YEAR.MONTH.2... YEAR.MONTH.42, etc. Those releases should be considered as milestones for the next stable one.

The changes made are tracked in the [CHANGELOG](https://github.com/eclipse-sirius/sirius-components/blob/master/CHANGELOG.adoc) where you can find a fine grain list of all the API breaks, new features, bug fixes and various improvements.

**Magic connector**

<figure>
<blockquote cite="https://www.youtube.com/watch?v=0p_1QSUsbsM">
It's a kind of magic<br/>
It's a kind of magic<br/>
A kind of magic (No way)<br/>
One dream, one <b>CONNECTOR</b><br/>
</blockquote>
<figcaption>—<i>Almost</i> Queen, <cite><a href="https://www.youtube.com/watch?v=0p_1QSUsbsM">A Kind of Magic</a></cite></figcaption>
</figure>

![Connector](https://docs.obeostudio.com/2022.01.0/img/MagicConnector.gif)

A new _"Magic Connector"_ tool is available on diagrams. It provides an alternative way to create edges between diagram elements:

1. choose the generic `Connector` tool from the source node’s palette
2. select the target node
3. choose which of the compatible tools to apply in the menu appears. If there is only one compatible tool, it will be applied automatically.

**DnD for Unsync diagram**

<figure>
<blockquote cite="https://youtu.be/ALanRqbNSvI?t=895">
Accepts she's out of sync<br/>
She's out of sync (sync)<br/>
She's out of sync (sync)<br/>
She's out of sync<br/>
</blockquote>
<figcaption>—Devo, <cite><a href="https://youtu.be/ALanRqbNSvI?t=895">Out of sync</a></cite></figcaption>
</figure>

Since the [2021.10.0](https://docs.obeostudio.com/#_version_2021_10_0) release, it is possible to create unsynchronized diagram with Sirius Web. It means a diagram which may not display all elements provided by the studio, but only the elements that the user selected.
At that time we added support for deleting view without deleting the corresponding semantic element (aka "Delete from Diagram") for unsynchronized diagrams.

![image](/img/2022.01.0/deletefromdiagram.png)

It is now also possible to drag semantic elements from the explorer on a diagram. The concrete effect depends on how the target diagram is defined, but a typical case is to add a graphical representation of the dropped element on the diagram.

![DnD](https://docs.obeostudio.com/2022.01.0/img/DropFromExplorer.gif)

**Fit to Screen**

<figure>
<blockquote cite="https://youtu.be/PzilYDj2b9k">
Now it fits you good<br/>
Oh fits you good<br/>
Yeah fits you good<br/>
Oh fits you good<br/>
</blockquote>
<figcaption>—Bryan Adams, <cite><a href="https://youtu.be/PzilYDj2b9k">Fits Ya good</a></cite></figcaption>
</figure>

When a diagram is opened, a "Fit to screen" is automatically performed to ensure all its content is visible. Previously, depending on the coordinates of the elements it could happen that not all of them were visible on open.

![Fit to screen](https://docs.obeostudio.com/2022.01.0/img/FitToScreenOnOpen.gif)

**Stylish studios!**

<figure>
<blockquote cite="https://youtu.be/-CmadmM5cOk">
'Cause we never go out of style,
we never go out of style
</blockquote>
<figcaption>—Taylor Swift, <cite><a href="https://youtu.be/-CmadmM5cOk">Style</a></cite></figcaption>
</figure>

Release after release we continue to improve the web studio definition capabilities.

Nodes can now have a dynamically computed size (using `Size Expression`) which depends on the current state of the semantic model. If the expression is present and produces a positive integer, it will be used as both the width and height of the node, in pixels. Currently it is not possible to compute different values for width and height.

![image](/img/2022.01.0/sizenodedef.png)
![image](/img/2022.01.0/sizenode.png)

It is now possible to define border nodes in web studio definition.

![image](/img/2022.01.0/bordernode.png)

And finally, it is possible to configure text style on labels: **bold**, _italic_, <u>underline</u>, ~~strike-through~~.

![image](/img/2022.01.0/style.png)

**Next**

The Obeo team has started a new iteration to preprare 2022.03.0, we focus on three topics:

- Support of **Component-like diagrams** with ports and bendpoints for edges,
- **Diagram user experience** to smoothly edit, move, reconnect and layout diagrams,
- And...(drum roll)... **Tables**! I am really enthusiastic about this one, we are cooking something really cool!

A detailed release notes for [2022.01.0](https://docs.obeostudio.com/#_version_2022_01_0) is available in our online documentation: [http://docs.obeostudio.com](http://docs.obeostudio.com).

As usual, all these changes are made available thanks to our loved customers sponsoring the Sirius Web open source project! Do not hesitate to join the party and become a Sirius Web supporter, it is as easy as sending me an email.

See you soon for the next Sirius Web and OCP ~~soundtrack~~ release!