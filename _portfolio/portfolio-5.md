---
title: "Drone fleet in a distributed environment"
excerpt: "A project for simulating the coordination of a fleet of drones in a distributed environment, developed in C#"
collection: portfolio
---

The project aims to create a solution that allows a fleet of drones (simulated) to coordinate their movements in an airspace, in order to avoid collisions.
Since this is an educational project for an exam, what is reported here is only a prototype of a simulated situation (i.e. without physical drones). However, what has been implemented are the communication aspects related to Distributed Systems.
In practice, the prototype created is already designed to be executed in a distributed environment, where the drone processes are deployed in different machines (or on the same machine, but in separate processes that communicate in the network through different ports).
In short, the idea is the following:

- imagine drones as very simple devices, without sensors and only capable of flying at a fixed height (the same for all), constant speed and in a straight line from a point A to a point B. Therefore, it is not expected that the drone is capable of doing complex things such as changing direction, stopping, "seeing" other drones with sensors, etc.

- each mission corresponds to an actor (a process performed directly on the drone), which communicates with the others by exchanging messages,

- when a drone wants to take off to complete a mission, before taking off it executes a distributed algorithm that allows it to:

- know all the other active missions in the airspace;

- negotiate with the other waiting drones to schedule departures in order to avoid collisions.

All of this was implemented in the C# language (.NET 6), making extensive use of the AKKA.NET framework to manage communication via messages.