# Decoupled Modules - A True Modular Application Development Framework

## The Problem

Modular application development promises code-reuse and allows high app-development efficnency. Inside a modular application architechture, at some point the software modules must connect to each other and exchange data in some forms, and the developer must decide the mechanism and the format to be used at the interfacing point between the modules for the data exhange. For tiered application, this could be a Entity Framework that objects that can be serialised when they are exchanged between the tiers. For distributed Web applications, data exchange are based on messaging using XML or Json that allows structured data to be exchanged. 

The problem is, at this point, the data exchange would be application dependent and vendor/implementation dependent, that is, not only the data is now fixed and cannot be easily changed, the associated code for parsing the data at the all involved components are tired to the Entity Framework or the XML/Json schema. In software design terms, this is called "tight coupling" which means inflexibility in software design. In the case of modular application development, if someone decided to change the data format all connected parties need to make changes accordingly. That's why most the modular application frameworks are evloved around a central vendor, typically it is who controls the the design of the data exchange format, and all the software components used in a framework are centrally developped and controlled by this vendor. 

It is desirable if an application can be assembled in such a way where the modules are independently developped and are interchangeable. Using the analogy of changing tyres for a car, we need a simple standard for connecting the two, as simple as nuts-and-bolts, rather than having a milion ways of connecting.

## Project DeMo ("The Solution")

The key to solve the above problem is the connecting points of the modules need to be "universal", meaning the interface between modules must not be tied to one specific data type or structure, and the chanllenge is how can this universal connecting mechanism is truly universal and can be used to connect everything. 

That is the goal of this GitHub project, "Decoupled Modules" ("DeMo") - a framework that has an universal connecting mechanism for independently developped modules to connect and form functional easy-to-maintain applications. DeMo is also a reposite of such modules which are open-sourced so people can take away and modify to suit his or her needs.

The key to this module-connecting mechanism is an "universal data format" called Recurrsive Delimited Array (RDA). Unlike XML and Json, RDA is schema-less and can contain and transport arbitorily complex data. Using RDA as the data exchange container means at the modules' interfacing point, the application framework does not impose a specifice data structure and allows unrestricted data exchange between connected modules. Compared to the other component-based modular application framework, Mortar allows independently developped and interchangeable modules from different vendor to work together in an app, which means greater code sharing and reuse in app development.

