# beseated

## Purpose

A sample repository where I plan on looking at bad practices in software and ways I think would improve upon these designs.

This is a congolmerate of bad practices I've seen on projects that have been aggregated into a single source. It doesn't represent all of
of the bad practices; merely the ones I find interesting or most annoying.

The basic design is going to contain at least the following elements:
+ HTML / Javascript frontend -> C# Web API -> Service Layer -> Data Access Layer -> Datastore
+ Database layer will expose all tables (yes join tables too!) and have the poor man's audit components to each table (CreatedBy, CreatedOn, UpdatedBy, UpdatedOn)
+ Service layer will be responsible for _everything_: authorization, building view models with lookup values and any business logic
+ Anemic models where all behavior exists in the services
+ .NET Standard (with looks to refactoring towards .NET Core)

Eventually, I would like to use this code to refactor into patterns that I want to play with as well, first and foremost event sourcing.

## Business Need
The year is 1999; the digital revolution has yet to set it's teeth in the restaurant business and all the floorplans are being
maintained by a hostess with a marker. GreatFoods, Inc has come along and wants an application which keeps track of the parties that are waiting,
that can assign them to a table, estimate wait times, etc.

## Terms

Here are the following terms that I use and what they mean.

+ Party - A group of people. 
+ Server - A restaurant worker who is waiting on a party
+ Table - A location where a party can seat and eat a meal... or simply camp and waste a server's time.
+ Section - A group of tables
+ Table Layout - A map of how the tables are setup and sectioned within the restaurant.
+ Floorplan - A table layout assigned to a shift that has section assignments to servers.
