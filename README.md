# A Vendor-Neutral Modular Application Development Framework

## The Problem

All no-code or low-code application frameworks these days are using modular development approach whereby the applications are composed using a collection of collbrative (and most importantly reusable) software components. Modular application architecture promotes code-reuse and allows high app-development efficnency.

At some point these software components must connect to each other and exchange some form of data. The application developer must decide the format to be used at the interfacing point between the modules, for the data exhange. Typically, the developer would choose to use an "open" data format such as XML or Json, and desing a schema for the data needs to be exchanged. The problem is, at this point, the data exchange becomes vendor dependent (on whoever defines the schema). Not only the data is now fixed and cannot be changes, the associated code for paring the data at the all involoving components are tired to the schema. In software design terms, this is called "tight coupling" which means inflexibility in software design.

As the result, most the modular application frameworks are evloved around a central vendor, typically it is who controls the the design of the data exchange schema, and all the software components used in a framework are centrally developped and controlled by this vendor. It is desirable if an application is assembled in such a way where the modules can be independenly developped and are interchangeable - just like we can change a car's tyres from different vendor. 

## Project Mortar ("The Solution")

The key to solve the above problem is the connecting points of the modules need to be "universal", meaning the interface between modules must not be tied to one specific data, and that is the foundation of this GitHub project, the Modular Application Framework, is based on.

Mortar utilizes the simple and flexible "universal data container" called Recurrsive Delimited Array (RDA) for the connected modules to exchange data. Unlike XML and Json, RDA is schema-less and can contain and transport arbitorily complex data. Using RDA as the data exchange container means at the modules' interfacing point, the Mortar application framework does not impose a specifice data structure and allow unrestrict data exchange between connected modules. Compared to the other component-based modular application framework, Mortar allows independently developped and interchangeable modules from different vendor to work together in an app, which means  greater code sharing and reuse in app development.

