1. sceneDelegate vs AppDelegate
2. http://studentdeng.github.io/blog/2014/08/29/ios-architecture/

WWDC 2014
Core iOS Application Architectural Patterns (session 224)
Time to look at the festival this year, a couple of WWDC session. A brief summary, respectively.

This Session is mainly about the iOS framework uses the most common mode of Cocoa, but a lot of framework, there's No need to worry about here, if you don't learn to understand the basic model, you will find many things are common.

The Session was relatively simple, review and consolidation of the iOS Classic mode.

Target / Action
consistent way to connect controls to custom logic

Control is that regardless of class, a Button or a BarButtonItem, are all through this model that will be used to control and custom logic connected.

Responder Chain
Handle events without knowledge of which object will be used

. [touch event Responder Chain] (responder Chain p.ng) Responder Chain most common application is to deal with Motion event.

For example, if a touch events with a View to deal with, then move up to View Controller handling, continued to climb. event by a Chain to deal with, this approach has many benefits. We don't need every event is given a specific object to deal with, but rather by a line to deal with, and ultimately, who is responsible and whether they need to respond by the response of the object itself to decide.

Composite
A group of manipulate objects as a single object

Think of View hierarchy, when moving the SuperView Sub view will follow a move. The things we take for granted, is behind the mechanism.

Delegation
Customize behavior without subclassing

This doesn't need to say more, but if there are already some development experience, sometimes run into some problems, with some thought to hack, flexible problem, often is caused by the bug causes. reasonably straightforward, often using standard models to produce a healthy and fit team code.

Data Source
Customize data retrieval without subclassing

essence and Delegation as well.

Model View controller
Provide organizational structure to focus responsibilities

Long stay is also a problem. reasonably segregation of duties, with a clear structure.

This Session is basic, but not without value, let me to brush up on some Cocoa's basic model. The need for greater clarity.
