# solv.us

## What is solv.us?
Solv.us is a collection of open-source, web-based & code-oriented software tools for VJing & controlling interactive installations. It enables you to use the power of the web and existing frameworks for it like [three.js](https://threejs.org) in the context of live events, both in the physical word and online.

## Why?
Working as a creative webdeveloper, I made the following observations:

- **Existing creative software for creating live event content is expensive and often not web-friendly.**
The popular VJ software Resolume and creative software environments MAX, TouchDesigner and Isadora, among others, are closed source, expensive, and not oriented to web technologies.
- **The web as a platform is more powerful than ever before and has a rich range of tools for content creation.**
An increasing number of web APIs are increasingly making websites function as full-fledged programs, without users having to go through an installation process like native applications. In addition, frameworks such as Three.js make it accessible to create complex 3D visualisations in the browser.
- **There is no easy way to use those tools for live events.** Setting up a server and integrating hardware is a lot of work that detracts from the creative process, while the requirements are similair for many projects.
- **We will increasingly experience live events via the web.**
More and more large-scale online events are taking place, such as Travis Scottt's online Fortnite concert. But combinations of digital and physical are also becoming more common, such as K / DA's Augmented Reality performance.

solv.us is designed as a general framework for these requirements, so you can focus on the fun parts of creative coding and use it in a live environment.

# Design

<p align="center">
<img alt="A diagram of solv.us' elements: A server, User Interface, Stages and connected clients" src="diagram.png">
</p>

### Server
The server is the heart of solv.us: it manages MIDI devices, media files, time, and the networking aspects of solv.us. It is written in TypeScript, a superset of JavaScript, and runs with the Node.js runtime. The choice for Node.js has two reasons. First, it has an event-driven architecture capable of asynchronous I/O, meaning that it has high scalability and throughput for application like solv.us that require a lot of real-time communication.

Seconds, JavaScript is also the language of browsers, and by unifying development around a single programming language, rather than different languages for server- and client-side scripts, it will hopefully make things easier for other developers.

### User Interface
The solv.us UI is the interface where you set up and control your project. It contains a workspace that is customizable with the elements that you need for your performance. The drag & drop system does not make a lot of sense yet in this stage of the project, due to the limited amount of components. But as I can imagine this library slowly growing over time, this hopefully will come in handy.

The colors are chosen to be easy on the eyes in a dark environment, while still highlighting the important elements like buttons with enough contrast. The used font is [FiraCode](https://github.com/tonsky/FiraCode), a monospaced font with ligatures for easy readability. 

### Stages
Stages are virtual or physical places that can contain different content and code, receiving events that it can react to. Since solv.us is a web-oriented tool, the most common form for a stage is to be a webpage. They are an abstraction that allow for more complex situations like media syncronization with different files over different places.

### Clients
Clients are instantiations of the stages. Think of it as the spectators. This can be a browser with a stage webpage opened, or a hardware device listening to a stage.

# Planning & Proces
## Week 1
- Created GitHub organization
- Set up repo structure
- Thinking out design philosophy

## Week 2
- Converted all old code for the server to TypeScript
- Refractored all old code into classes
- Experiments ( MIDI input -> Colors on a LED strip)
- Research into Resolume / Touchdesigner 

## Week 3
- Switched to a HTTPS server with auto-certificate generation
- Drag & Drop system for the UI
- Attempt at window management: failed
- Working Events on the server side

## Week 4
- Attempt 2 at window management
- New design system: colors, font, buttons, inputs, margins, paddings, etc.
- UI Components for event management, stage manager, & connected client windows

## Week 5
- Finished MIDI clock on the server side
- Finished MIDI mapping on the server side
- Updated solv.us landing page with new design system

## Week 7
- Redesigned standby screen for stages
- Finished 'client' code and released it as NPM package.

## Week 8
- Latest fixes, Documentation, Itch.io page, Video.


# PMI
+ I'm happy with the end-result, and used it in the seminar that followed Project Vrij. It proved to be useful there.
+ I learned a lot about releasing open-source software, especially about versioning, package management & bundling, and npm. 
+ I managed to stay (mostly) motivated and productive despite the circumstances

- The orginal scope of the project was too large / I was too optimistic about how much I could do on my own in these months.
- Corona limited the more physical manifestations/usage of the software.
- Writing clear documentation to help other developers understand your project was less harder than I though it would be. 

i I am interested in what other people working in the creative development field think about the project
i I'm curious to see how this software is going to change my work in the future 


## Team 26
Daan Korssen (Developer/Designer), student no. 3032555

