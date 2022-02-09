Sirius Web is & is not

Is:
a new web modeling framework pluggable with EMF,
a multi-user collaboration model server
a multi-user collaboration server

Is not :
A versioning system

Model server

A default EMF implementation is provided

Collaborative modelling, Simultaneous change, stay semantically correct
Share with git

Capability to provide your own kind of models (ontology…)
Take care of :
load and retrieve model instances
modify model elements
subscribe to changes
synchronize multiple views
How does it scale?
Clarify maturity

Missing :
no command stack -> no undo/redo
Validation : trigger the validation and retrieve the results, EMF code validation.

What’s in there?

Sirius Web is :
Ready-to-use modeling framework to render modeling application in the web
Open source model client (diagram, properties, forms…) and model server components
Implemented using Spring Boot, GraphQL, React, Material UI

Projects browser
Project editor
Details view
Project context menu
Create a new Model in a project
Share project
Project owner & visibility
Project Teams
Share diagram
Diagrams

Several diagrams on top of one model

Edges , Nodes, Containers, Containers List
Shapes SVG + CSS

Editing : Palette, Direct edit (Missing content assist, inline validation) , Resize element, move element, (Missing copy/paste, undo/redo, context specific actions)

Ports + edges routing (Missing routing for edges)

Layouting : Auto-Layout, incremental layout (Missing alignment) + store layout

Zooming

Missing navigation, validation/error markers

Conditional style line width en fonction d’un paramètre du modèle

Create your studio!

Download domain model to show that it is an ecore

Create Class
Create Attribute
Change multiplicity
Create Enum
Direct edit type, referencing an enum
Show default EMF serialization
Validation ;(
Ecore models referencing other ecore models ?

No genmodel to define, no code generation, no generated code
Property view, live updated (name class, abstract class)
Zoom

Dark theme?
Share

Odesign support

Diagrams
Services + service call tools demo
Reusing existing components reduce effort and preserve your investments
Migration path

**I want diagrams in my own application!**

- Representations
  ** Diagrams \*** Display
  ** Edit
  ** Integrated where you want

- Studios
  ** Full web definition \*** Domain
  \*\*\* View

- Enterprise
  Private/public, server management, webhooks, LDAP/SSO...

- Developer
  SC
