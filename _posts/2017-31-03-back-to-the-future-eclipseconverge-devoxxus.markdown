---
layout:     post
title:      "Back to the Future"
subtitle:   "Eclipse Converge & Devoxx US "
date:       2017-03-31 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-02.jpg"
tags: [planet]
---
Last week, [Obeo](https://www.obeo.fr/en/) sent me to San Jose, California to attend the 1st [Eclipse Converge](https://www.eclipseconverge.org/na2017/) and [Devoxx US](https://devoxx.us/) which was really cool of them. It makes sense to co-locate those events as both involved Java developers and open source projects. I really believe that these communities have so many things to share that this week in California would be a great occasion to learn from each other.

![Back to the Future](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/back_to_the_future.jpg?raw=true "Back to the Future")

## Eclipse Converge
I started my week by attending [Eclipse Converge](https://www.eclipseconverge.org/na2017/), a one-day event dedicated to the Eclipse community and co-located with the IoT day.

![Eclipse Converge & IoT day](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/eclipse_converge_iot_day.jpg?raw=true "Eclipse Converge & IoT day")

The number of Eclipse committers present was amazing, which was particularly noticeable thanks to the Eclipse committer swag, a cool purple hoodie! 

![Eclipse Committer Hoodie](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/eclipse_hoodie.jpg?raw=true "Eclipse Committer Hoodie")

One thing I noticed is that this year for the first time, they have it in women sizes! This is one of those little things which helps our community to become more diverse!
Thanks Eclipse Foundation, I love it so much!

As all Eclipse events, it was a great moment of social networking, attending high quality talks, meeting the usual suspects and getting the chance to exchange with american Eclipse community members.

## Devoxx US
The day after, [Devoxx US](https://devoxx.us/) started! It was a new chance for me to meet this extended community, as this was my first Devoxx ever and no doubt Devoxx is a great event. 
Thanks to the Eclipse Foundation for having gathered 700 attendees from 31 countries in the same place during 3 days.
One of the important thing about Devoxx is that it is a vendor neutral event: not everything is related to Eclipse or a specific IDE, there's a much wider diversity of content. Thanks to this, I've been able to attend many different demos based on different IDEs. This allowed me to notice some interesting differences:

I loved the clean UI of VSCode,

I appreciated the templates and the zoom in IntelliJ that allow fluent live coding demos,

I was impressed by the [talk by Stevan Lemeur and Florent Benoit](https://www.eclipseconverge.org/na2017/session/how-provide-portable-developer-workspace-eclipse-che) and the easy setup of Eclipse Che thanks to CheFile and Factories! From just clicking on an hyperlink, it will provide you a complete IDE in your browser with all the tools, projects and source code you need. This opens a really cool possibility for open source projects who want to ease the effort to start contributing.

I discovered the new stuff that will be relased in June with the next Eclipse Oxygen version. Wayne Beaton from the Eclipse Foundation and Gunnar Wagenknecht from SalesForce did an interesting [talk](http://cfp.devoxx.us/2017/talk/RNK-9521/Developing_Java_Applications_with_the_Eclipse_IDE,_Neon_Edition) about all these useful projects existing or arriving: Code recommenders, ECLEmma, Graphviz editor, Improved UX with a better use of screen space (margins reduced, default styling...), support of Java9 and JUnit5, and a new Generic Editor becoming particularly useful combined with the Language Server Protocol.

![Eclipse Oxygen](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/eclipse_oxygen.jpg?raw=true "Eclipse Oxygen")

## Language Server Protocol
Until I heard about LSP, I did not realize how complex it is for language developers to get a good support and tooling of their language in all those different IDEs.
A really clear introduction to LSP was given by Sven Efftinge from TypeFox who explained the origin, the status and the potential of LSP for the Eclipse community.
![Language Server Protocol Explained](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/lsp.jpg?raw=true "Language Server Protocol Explained")
Thanks to this talk, I now understand better the power of the LSP. Open sourced by Microsoft for VS Code, the Language Server Protocol is the new trend for language editors. In a few months, Microsoft, Red Hat, Codenvy and many others started collaborating to implement it for VS Code, Eclipse, Eclipse Che, Emacs and even Gnome builder! Only open source can create this kind of synergy and cooperation. In Eclipse, it results in three new projects that will be released with the next Eclipse Oxygen :

[LSP4E](https://projects.eclipse.org/proposals/eclipse-lsp4e): provides integration of language servers conforming to the Language Server Protocol into the Eclipse IDE.

[LSP4J](https://projects.eclipse.org/proposals/eclipse-lsp4j): provides a reusable Java implementation of LSP. It implements the types as well as the communication, including serialization to and deserialization from JSON.

[Generic editor](https://bugs.eclipse.org/bugs/show_bug.cgi?id=497871): supports easily new languages.
For the next release, LSP will allow to get the same level of support for JS in Eclipse and VS Code. But even more when like me you are working on Domain Specific Language, this could be really powerful: imagine you're developing your own DSL and you easily get support for it in all the editors. This is possible now thanks to Xtext Core.
This is only the beginning, there are some remaining issues to solve around extensibility, creating a market place, supporting debug features... At the moment the LSP is dedicated to textual editors, I expect that one day it can be extended to graphical editors too!

## Lessons Learned
Open source allows to gather skilled people from different companies to develop together around a common goal. A conference like Devoxx allows you to advance your personal knowledge and to become an innovation agent in your own company. The organizers define it as a "Conference for developers by developers". I attended many talks that highlighted how important it is in our domain to learn from our peers. [Marko Gargenta](https://medium.com/@markog) in his talk about [Peer Learning](http://cfp.devoxx.us/2017/talk/JVD-8929/Peer_Learning) narrated his experience at Twitter and explained that there are different ways to share knowledge, classically by organizing techie classes but not only. One of the interesting things I remember from his talk is the need to share knowledge about technical aspects, but also about the company culture, for example by recounting what he named _War Stories_.
Ryan Sonnenberg talked about what they did to disseminate the knowledge at Uber while they scale. From his point of view, best practices shared by code reviews do not scale as an individual reviewing code cannot disseminate knowledge fast enough. The main point for him is to hook into the build system in order to enforce patterns and so eliminate the repetitive work and cumbersome manual processes: use static analysis, [FindBugs](http://findbugs.sourceforge.net/), [Infer:Eradicate](http://fbinfer.com/docs/eradicate.html), [checker framework](https://github.com/typetools/checker-framework.demos/tree/master/presentations/2017-DevoxxUS)...
I attended three other good talks sharing best practices from the battlefield: 

[Ten simple rules for writing great test cases](https://www.slideshare.net/StevePoole/ten-simple-rules-for-writing-great-testcases-devoxx-us) by Stuart Marks & Steve Poole: Rules to maximize your effort & protect investment in tests
![Ten simple rules for writing great testcases](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/ten_simple_rule_for_wrinting_testcases.jpg?raw=true "Ten simple rules for writing great testcases")

[Prototyping mindset](http://haughtcodeworks.com/blog/software-development/prototyping-mindset/) by Marty Haught: Invoke YAGNI whenever it makes sense and reduce the complexity of your solution!

[Test Lessons from the field](https://www.eclipsecon.org/europe2016/content/testing-eclipse-plug-ins-lessons-field) and [Effective Unit Testing](http://cfp.devoxx.us/2017/talk/RQL-8052/Effective_Unit_Testing) by Elliotte Rusty Harold, Simple and easy to follow advices for every day that could be summarized by: 
- Separate your Eclipse/Non Eclipse code, your GUI/Non GUI projects, 
- Test also your configuration files (plugin.xml, MANIFEST.MF, plugin.properties...), 
- One of the most obvious advice but definitely worth to be heard when you found a bug first write a test and then fix the bug.
- And finally use Continuous Integration and code coverage tools like Cobertura or Jacoco.

## Build
Build was also the topic of several excellent talks. I always use Maven just from habit and not really because I love it. That's the case for most of us, we use it and hate it. Andy Gumbrecht proposed an	intriguing ignite session by declaring [I do not hate Maven](http://www.tomitribe.com/blog/2016/06/i-do-not-hate-apache-maven/). He explained that it is not useful to fight against Maven, when you have to do something with it just do it the Maven way. For him your pom hygiene is the key, it should read like a book, keep it clean and tidy. Manage your environment at the highest possible level in your top parent and invest in global properties to control it. Manage versions and not scopes. Groovy gives the ability to do anything at any stage of the build, so use it.
And when you have a Maven issue, just remember that Google is your friend!

I took the time to explore what other build systems can offer. An excellent tools in action was proposed by Baruch Sadogursky & Oleg Šelajev about [Maven vs Gradle](http://cfp.devoxx.us/2017/talk/XFT-7496/Maven_v_Gradle:_Dawn_of_Project_Automation), it was mostly a demo comparing the tools on the same project. At the end, my impression was that both provide the same features, it is more a matter of taste: Maven due to XML is very verbose and Gradle feels more readable/maintainable.
For the ones using Eclipse like me, using the [M2E](https://www.eclipse.org/m2e/) plugin can help, for Gradle lovers, a thorough [overview of the Gradle tooling available in Eclipse](https://github.com/diffplug/gradle-and-eclipse-rcp) was done by Ned Twigg. To go further, and for whom performance matters, Ryan Sonnenberg during his session [Building at Uber scale](http://cfp.devoxx.us/2017/talk/SSI-8355/Building_at_Uber_scale) talked about [OkBuck](https://github.com/uber/okbuck), a plugin to use [Buck](https://buckbuild.com/) build system on Gradle project.

## JDK8
I took time also to inspect some classical APIs. My first astonishment is that : Yes it is possible to do a 1h talk only about 
[Optional](https://stuartmarks.files.wordpress.com/2017/03/optionalmotherofallbikesheds-devoxxbe2016.pdf)! Stuart Marks did it and it was pretty interesting. Going through examples, he declaimed the following seven rules which for sure have to be pinned to my wall :
![Optional - The Mother of all Bikesheds](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/ten_simple_rule_for_wrinting_testcases.jpg?raw=true "Optional - The Mother of all Bikesheds")
One more talk I found useful is the one about [comparing the different Java Collections libraries](http://cfp.devoxx.us/2017/talk/PEV-2089/Collections.compare(JDK,_Eclipse,_Guava,_Apache...);). You know this doubt you have sometimes: should I use Java Collections? Guava? Eclipse Collections? Which one would be the most effective in my situation? The following summary can help you take a decision:
![Collections.compare](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/collections_compare.jpg?raw=true "Collections.compare")
Stuart Marks again demonstrated the new features of collections in Java 8, as well as what’s coming in Java 9: [Collections Refueled](https://www.youtube.com/watch?v=LgR9ByD1dEw).

## JDK9 
As you guess, one of the hot topic during Devoxx was the new Java 9! Definitely, the next stop for the Java developers will be the upcoming release of the JDK9, on July, 27th. Notice that finally Oracle adjusted the versioning scheme: they will no longer be named 1.x!
There were lots of Oracle talks about Jigsaw, the new modular way of coding. In fact, this is not that exciting, even more when you are working in the OSGI world as I do since many years now. For most Java developers, this seems mostly like something which looks painful as it might break everything.
Trisha Gee did a great talk [Anticipating Java 9 functionnality & tooling](https://www.youtube.com/watch?v=96vce1qd0QY) presenting what we could expect more from Java 9 and demonstrates how IntelliJ already support it. Worth mentioning that Eclipse also already has support for JDK 9 thanks to the great work done by the IBM JDT team. They announced a special Eclipse update available at the end of July to support it the day of the JDK9 official release.
So what are those little and big things I await for Java9 ?
* Better everything: memory, performance, doc, faster compilation...
* New methods on stream API: takeWhile/DropWhile, List.of/Set.of/Map.of/Map.ofEntries
* HTML5 Javadoc
* Javadoc search
* Private static methods available in interface
* @Deprecated(since, forRemoval)
* New process API
* Java9 REPL: JShell
* Flow API which means that reactive programming is an important programming paradigm now and is really here to stay. You do not know yet what it means? Have a look at the good introduction by Venkat Subramaniam about [Reactive Programming in Java](https://www.youtube.com/watch?v=weWSYIUdX6c).

## Modern web
I am not a web developer but I attended few interesting talks about modern web development as well, my top 3:

[Binge streaming your web API](https://www.youtube.com/watch?v=VT4xsDCeDxE) by Audrey Neveu & Guillaume Laforge where I discovered the principle of Server-Sent Events and a great use of JSON patch.

[Angular2 for Java dev](https://www.slideshare.net/yfain/angular-4-for-java-developers) by Yakov Fain which demystifies the Angular framework.

[Is your JavaScript ready for enterprise ?](http://cfp.devoxx.us/2017/talk/NWB-0408/Is_Your_JavaScript_Ready_for_the_Enterprise%3F_What_Does_That_Even_Mean%3F) by John Brock who tought me to resist to the hype, to rediscover HTML5 and to choose between all the JS frameworks and libraries options.

## Homeworks
As usual coming back from a conference, I still have some homework to do now, I will just share what will be the next stops for me, I should have a look at:

[Mockito 2](https://github.com/szczepiq/mockito-devoxx-2017) : I have to re-try this popular mock framework which can be used in conjunction with JUnit to write even cleaner tests.

[Cucumber & Citrus](https://github.com/christophd/citrus-demo-devoxx-us) : was not able to attend this one, I am waiting for the video. 

[JUnit5](http://cfp.devoxx.us/2017/talk/ZCD-4979/JUnit_5_-_The_New_Testing_Framework_for_Java_and_Platform_for_the_JVM) : one of the best news of this week, a complete redesign of the JUnit framework, that will arrive soon and well [integrated in Eclipse](https://www.eclipseconverge.org/na2017/sites/default/files/slides/Embracing%20JUnit%205%20with%20Eclipse.pdf) for the Oxygen.1 release for this fall. 

## Open your mind
To conclude, DevoxxUS was really impressive in terms of technical contents. There were also lots of fun and unexpected sessions. I laughed out loud during the session about [the Business of Technology Business Technology](http://cfp.devoxx.us/2017/talk/OTY-5246/The_Business_of_Technology_Business_Technology) by Chet Haase and the [Java Posse](http://javaposse.com/) live podcast and moreover I learned diverse things like [home brewering](http://cfp.devoxx.us/2017/talk/YOX-8173/Developer's_guide_to_HomeBrewing..._) or [how to not restore a VW bus](http://cfp.devoxx.us/2017/talk/FEI-0558/How_NOT_to_restore_a_VW_Bus).
Finally, I opened my mind to new horizons with great sessions about experiments around [AI design](http://cfp.devoxx.us/2017/talk/NHF-2672/Personality_Is_the_New_Ringtone:_Experiments_in_AI_design), [deep learning](http://cfp.devoxx.us/2017/talk/OHB-4306/Deep_learning_in_biomedicine:_challenges_and_opportunities), [quantum computing](http://cfp.devoxx.us/2017/talk/VUB-9615/New_Computer_Architectures_:_Explore_Quantum_Computers_&_SyNAPSE_neuromorphic_chips)!
No doubt now I have to attend the other Devoxx in France, in Belgium and in US again. If you have the chance to attend [Devoxx France](https://www.devoxx.fr) next week, come by to say ‘Hi’ to the Obeo guys at the [Eclipse Foundation booth 26](https://www.devoxx.fr/assets/images/plan_stands.jpg). See you there in the future!
![Where we're going we don't need roads](https://github.com/mbats/mbats.github.io/blob/master/img/devoxxus/roads.jpg?raw=true "Where we're going we don't need roads")