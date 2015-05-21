# Documenting Software Architectures

Notes on the book [Documenting Software Architectures: Views and Beyond](http://resources.sei.cmu.edu/library/asset-view.cfm?assetID=30386).

## Contents

- [Overview](#overview)
    - [Why Document Software Architecture?](#why-document-software-architecture)
    - [Quality Attributes](#quality-attributes)
- [Architecture Views](#architecture-views)
- [Architecture Styles](#architecture-styles)
    - [Module Styles](#module-styles)

## Overview

The book attempts to answer the question:

> How do you document an architecture so that others can successfully use it, maintain it, and build a system from it?

### Why Document Software Architecture?

A good architecture is useless if people using it don't know what it is, can't understand it, or misunderstand it and apply it incorrectly. This means the time spent designing it has been wasted.

It delivers value to developers, deployers, testers, and clients.

- Education: New team members, third party developers, or product owners.
- Communication: Explaining how a feature is implemented or discussing an approach for a new feature.
- Analysis: Provides a view of what needs to be tested when modifying or adding new code. Ensures features are implemented in accordance with the system's [quality attributes](#quality-attributes).

### Quality Attributes

Quality attributes such as performance, reliability, security, and modifiability are important in almost all systems.

Architecture is where these concerns are addressed.

Different quality attributes require different attention. For example:

- Performance: Exploit parallelism
- Security: Identify where unauthorised intrusion will do the most damage
- Modifiability: Separate concerns so changes are isolated

## Architecture Views

Views are the core concept associated with architecture documentation.

> Documenting an architecture is a matter of documenting the relevant views then adding documentation that applies to more than one view.

A documentation package can be composed of one or more view documents and documentation that explains how the views relate to one another.

To document a bird's wing you may require views of: feathers, skeleton, circulation, a muscular view etc. None of these *are* the architecture, but together, they *convey* the architecture.

Different views expose different quality attributes and support different goals. For example a *layered view* tells you about portability, a *deployment view* lets you reason about performance and reliability.

The documentation for a view contains:

- Primary presentation, usually graphical, showing primary elements and relations.
- An element catalog (key) that defines the presented elements.
- Specification of the elements' interfaces and behaviour.
- Rationale and design information.

The documentation that applies to all of the view contains:

- Introduction to the entire package.
- Constraints and rationale for the overall architecture.
- Management information required to maintain the package.

## Architecture Styles

There is no fixed set of views that is appropriate for every system. There are some broad guidelines which can help:

- How the software is structured as a set of implementation units.
- How the software is structured as a set of elements that have runtime behaviour and interactions.
- How the software relates to non-software structures in its environment.

The are three categories of styles in the book:

- [Module styles](#module-styles)
- Component-and-constructor styles
- Allocation styles

### Module Styles
