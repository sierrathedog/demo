# Snap-X

Snap-X is a modular application development framework that allows independently developed software modules to connect and collaborate inside the framework. Snappable-based modular application is easy to develop and allows greater code sharing and reuse freedom.

It has the following API for implementing "open-market and reusable" modules. The key to this API is using the IRda universal container for exchanging data between an initiator and a responder. Foldda's Snap-X Connect is a product that demonstrates how the framework and the modules work.

## Snappable: Snap(initiator) => Engagement  //a context of two-module engagement
### Engagement (Snappable initiator, Snappable responder)

### Engagement: Request (IRda request) => ResponseHandle  //an info exchange between the engaged modules
## ResponseHandle: Pull (IRda condition) => IRda response
## ResponseHandle: Pull (IRda condition) => IRda response
...
### Engagement : Release();

## The Problem

Modular application development promises code reuse and allows high app development efficiency. Inside a modular application architecture, at some point, the software modules must connect to each other and exchange data in some forms, and the developer must decide the mechanism and the format to be used at the interfacing point between the modules for the data exchange. For tiered applications, this could be an Entity Framework in that objects are serialized for being exchanged between the tiers. For distributed Web applications, data exchange is based on messaging using XML or JSON for exchanging structured data. 

The problem is, at this point, the data exchange would be application-dependent and vendor/implementation dependent, that is, not only the data is now fixed and cannot be easily changed, the associated code for parsing the data at all involved components are tired to the Entity Framework or the XML/JSON schema. In software design terms, this is called "tight coupling" which means inflexibility in software design. In the case of modular application development, if someone decided to change the data format all connected parties need to make changes accordingly. That's why most modular application frameworks are evolved around a central vendor, typically it is who controls the design of the data-exchange format, and all the software components used in a framework are centrally developed and controlled by this vendor. 

It is desirable if an application can be assembled in such a way that the modules are independently developed and are interchangeable. Using the analogy of changing tyres for a car, we need a simple standard for connecting the two, as simple as using standardized nuts-and-bolts in the mechanic world, rather than having a million ways of connecting.

## Project DeMo ("The Solution")

The key to solving the above problem is the connecting points of the modules need to be "universal", meaning the interface between modules must not be tied to a specific data type or structure, and the challenge is how can this universal connecting mechanism is truly universal and can be used to connect everything. 

That is the goal of this GitHub project, "Decoupled Modules" ("DeMo") - a framework that has a universal connecting mechanism for independently developed modules to connect and form functional easy-to-maintain applications. DeMo is also a repository of such modules which are open-sourced so people can take away and modify them to suit their needs.

A central piece to this module-connecting mechanism/solution is a "universal data format" called [Recursive Delimited Array (RDA)](https://github.com/sierrathedog/rda). Unlike XML and JSON, RDA is schema-less and can store and transport arbitrarily complex data. Using RDA as the data exchange container means at the modules' interfacing point, the DeMo framework does not impose a specific data structure and allows unrestricted data exchange between connected modules. Compared to the other component-based modular application framework, DeMo allows independently developed and interchangeable modules from different vendors to work together inside an app, which means greater code sharing and reuse in app development.

