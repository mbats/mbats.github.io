---
layout:     post
title:      "Joy"
subtitle:   "Sirius 4.1 is Out! What's inside?"
date:       2016-10-24 08:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-02.jpg"
---

This week I am participating to [EclipseCon Europe](https://www.eclipsecon.org/europe2016/) to present what’s new in [Eclipse Sirius](https://www.eclipse.org/sirius/) 4.1.

![](https://lh3.googleusercontent.com/xP9yG2rBajXphda-MNbbPdCA2WRZ4K2oNZJGYgE9T3JIgb9X1EJpj47JSNQf4sXW5dAUgfeOMbbS0GY_ROu9eqGDDuFH1Az5WL4XXPnfVd41jL2UQchSOKXmu2ZWhrKtoepUNErw){: .center }

What I feel like on monday morning: Joy!

![](https://lh6.googleusercontent.com/VnC_vS4-_9NfxS2OQF_a0bdS8wlakki-OvmoyvMFhf9lwjt8YGhNhw8iZLp9adgv2f3Y-WsniNoXp3XMYP8CuZ_6eWJ5jSDGqDr2zEyBVGD25uaGHKkjXR6OqTOLGPGxe81K7Y5f){: .center }

On Monday evening I’ll be in Ludwigsburg for EclipseCon! This one is little special as it will be my first one as an official Sirius committer.

I am really happy to introduce you to the new features of the 4.1 release, especially what we did to improve the specifier experience:

*   Pre-registered service class: starting from Sirius 4.1, by default when you create a new Viewpoint Specification Project, a service class is pre-registered.

![](https://lh5.googleusercontent.com/cX5w3vYba1tzBtgekaSrGLUarRiLLYcoQbz9NfLaBJHYvAb0cLd5eS1SImXLR-v7cn2LFIdMPVVzllx7dmdTm3j4dvFs3jPymt1S-Hy9UymLPDOYQFLpN1E0c6gk6Kg6oUVlMTKh){: .center }

*   Improve the selection of deeply contained Viewpoint Specification Model elements: in a style property customization, the "applied on" field was used to open a popup with all styles of the VSM. As they are identified by type and color (e.g. square blue) a lot of entries are identical, making it difficult to select the correct one. Now it is more user friendly as the mapping container of the style is also presented.

![StyleCustoSelection.gif](https://lh3.googleusercontent.com/oFtY03_FLNu36mYFhX9AcIJzehqDRYi0CARnBWkDz0CwQmIyiuFjgf3U259jqMLcYFA4bShuGDPIbOxMT9XQb1j1WZ3KOqmGzI1sg6PZEkrjj1NF6R0lL_sNqCb8EXmvuEINM2sE){: .center }

*   Properly configured I18N: we have completed our work on the internationalization, with the runtime strings being properly externalized. As a result, you can specify keys in your VSM and using a properties file you can have translated labels in your user interface, here in Japanese. Since Sirius 4.1, new Viewpoint Specification Projects are properly configured for I18N.

![](https://lh4.googleusercontent.com/0iiYFsNDKE-p8QUy1GEfsDQOJiuSbPbKqzF0L9MkclOwFPvtuh5rq6pzSrirutX9O8oOz4Z8O8ameQqkhUbIQTPQA6T_dn3coeDlPfiQZ0YC5wv9BGic532wJZFajWn47_7fNKyQ){: .center }

*   Specifier editor for properties view description: we provide also the completion, and contribute a new simplified reference widget.

I invite you to join the Sirius team tomorrow morning for the [Sirius workshop](https://www.eclipsecon.org/europe2016/session/sirius-workshop-lets-create-graphical-modeling-editor-robot) to experience in live all these new improvements. See you there!