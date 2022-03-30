---
layout: post
title: "Meet Sirius in the browser"
subtitle: "Your web modeling tools best friend"
date: 2022-03-30 10:00:00
author: "Mélanie Bats"
header-img: "img/post-bg-02.jpg"
tags: [planet]
---

_TLDR; This post is for you if you want to build web-based graphical modeling tools.
[Eclipse Sirius](https://www.eclipse.org/sirius/sirius-web.html) is an open source project to create domain-specific modeling workbenches._

At this point, if you are not aware of "modeling and domain specific blablabla", you might wonder _"What does it mean and why should I care?"_.

**Give semantics to your drawing...**

That is simple, you have **data** (and I am pretty sure you have some, everyone has data nowadays :)).

![Data Pipeline](https://imgs.xkcd.com/comics/data_pipeline.png)

And you want to **represent** and **edit** them in a visual way: diagram, table, forms, dashboard... You have so many ideas! You can already visualize them in your head! But you also want to **utilize** the information stored in your dataset...

- First option, you can use sheets, databases, low code platforms to represent and store your data and you can map your data to charts, forms... This is what you do with tools like Excel, Google Sheets, Airtable, and many low code tools… but there is no way to represent them on a diagram ;(
- Second option, you can represent your data graphically... thanks to tools like Miro or draw.io... but then you are stuck! It is just a drawing, you cannot leverage the semantics of your data ;(

"Holy crap... what could I do ?"

Come here... I have a secret to share with you: you should use [Eclipse Sirius](https://www.eclipse.org/sirius/sirius-web.html)!

Sirius allows you to **represent your data**, **map them to graphical representations** and **take advantage of your data's semantic**!

**What is Sirius Web? And OCP?**

Sirius has two flavors:

- **Sirius Desktop**: to create modeling workbenches based on the Eclipse platform,
- **Sirius Web**: to create cloud-ready modeling workbenches.

![image](/img/siriusweb/architecture.png)

Furthermore, as we are very greedy, we provide the [Obeo Cloud Platform (OCP)](https://www.obeosoft.com/en/products/obeo-cloud-platform) as Sirius Web topping. OCP is a set of Cloud-based products to easily build and deploy modeling studios to the web for enterprise use cases. We offer [Obeo Studio](https://www.obeosoft.com/en/products/obeo-studio) to create graphical modeling solutions that can be used collaboratively from a web browser.
Obeo Studio is built as an open-core product relying on Sirius Web: it is a Sirius Web build extended with Enterprise features, to deploy on public, private clouds or on premise and including support and upgrade guarantees.
One more option for you is to use the components from Sirius Web and OCP to integrate in your own application.

So you are asking yourself _"Ok, I got it but what can I do concretely?"_

**Define your domain**

The first thing to do is to describe your data. You can use Sirius Web to define your concepts and how they are related to each other.

![image](/img/siriusweb/domain-start.png)

For instance, I need a tool to represent all the things I have to do.

I create a new `Domain` with the following concepts:

- `TodoList`: contains all I want to get out of my head :)
- `Objective`: my end goal
- `KeyResult`: how I know that my goal is achieved

![image](/img/siriusweb/domain.png)

An objective is associated with one or more key results.

**Map to visual representation**

The next step is to decide how you want to represent your data: you have to create a `View`. For my to-do list tooling, I decide to represent it with a **diagram**:

- a graphical _node_ for each concept I have: `Objective` and `KeyResult`
- an _edge_ `ObjectiveToKeyResult` to show which key results are associated with which objectives.

![image](/img/siriusweb/view2.png)

**Semantics forever!**

One last point (and I promise after that you can go back to normal activity), with Sirius Web you can also specify behaviors associated with your data. For instance, in my diagram I want to see what are the objectives I have checked and the ones that still need to be worked on.
I can describe a conditional style on my `Objective`:

- red when it is not yet completed,
- green when all the key results are set to `Done`.

![image](/img/siriusweb/studio3.png)

**Your studio is alive!**

What do you have to do next? Nothing! Just try your new dedicated tool! Sirius Web manages everything for you.
Without anything to deploy, I can create a new project and use the Domain and View that I’ve just defined, to create a `Todolist`, containing KeyObjectives and Objectives, and create a synchronized graphical representation.
I can create new objectives and new key results, set their attributes and so on.

![image](/img/siriusweb/studio.gif)

If I go back to my tooling's expectations, using Sirius Web I can:

- [x] **represent** and edit my **data graphically**
- [x] **enhance my dataset** thanks to **semantics**!

**Give it a try!**

If you want to try it by yourself, just create an account on our online demo: [https://demo.obeostudio.com](https://demo.obeostudio.com).
And if you have questions about Sirius Web or OCP, contact me!

As usual I am thankful to all our customers for their support of Sirius Web!
