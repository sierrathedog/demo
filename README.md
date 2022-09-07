# A Vendor-Neutral Modular Application Development Framework

## The Problem

All no-code or low-code application frameworks are using modular approach whereby the apps are composed using a collection of collabrative (and most importantly reusable) software components. Modular application architecture promotes code-reuse and allows high app-development efficnency.

Inside a modular application architechture, at some point the software modules must connect to each other and exchange some form of data, and an application developer must decide, based on the application's requirement, the format to be used at the interfacing point between the modules, for the data exhange. For stand-alone or tiered application, the developer would design a Entity object for being used at the interfacing. For distributed application, typically, the developer would choose to use an "open" data format such as XML or Json, and desing a schema for the data needs to be exchanged. 

The problem is, at this point, the data exchange has made the app vendor dependent, that is, not only the data is now fixed and cannot be easily changed, the associated code for parsing the data at the all involved components are tired to the Entity object or the XML/Json schema. In software design terms, this is called "tight coupling" which means inflexibility in software design. As the result, most the modular application frameworks are evloved around a central vendor, typically it is who controls the the design of the data exchange format, and all the software components used in a framework are centrally developped and controlled by this vendor. 

It is desirable if an application can be assembled in such a way where the modules are independently developped and are interchangeable - just like we can change a car's tyres that are made from different vendor. 

## Project Mortar ("The Solution")

The key to solve the above problem is the connecting points of the modules need to be "universal", meaning the interface between modules must not be tied to one specific data, and that is the design goal of this GitHub project - the Mortar Modular Application Framework.

Mortar utilizes the simple and flexible "universal data container" called Recurrsive Delimited Array (RDA) for the connected modules to exchange data. Unlike XML and Json, RDA is schema-less and can contain and transport arbitorily complex data. Using RDA as the data exchange container means at the modules' interfacing point, the application framework does not impose a specifice data structure and allows unrestricted data exchange between connected modules. Compared to the other component-based modular application framework, Mortar allows independently developped and interchangeable modules from different vendor to work together in an app, which means greater code sharing and reuse in app development.

