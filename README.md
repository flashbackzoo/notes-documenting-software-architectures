# Documenting Software Architectures

Notes on the book [Documenting Software Architectures: Views and Beyond](http://resources.sei.cmu.edu/library/asset-view.cfm?assetID=30386).

## Contents

- [Overview](#overview)
    - [Why Document Software Architecture?](#why-document-software-architecture)
    - [Quality Attributes](#quality-attributes)
- [Architecture Views](#architecture-views)
- [Architecture Styles](#architecture-styles)
- [Module Views](#module-views)
    - [Decomposition Style](#decomposition-style)
    - [Uses Style](#uses-style)
    - [Generalisation Style](#generalisation-style)
    - [Layered Style](#layered-style)
    - [Aspects Style](#aspects-style)
    - [Data Model Style](#data-model-style)
- [Component-and-connector Views](#component-and-connector-views)
- [Allocation Views](#allocation-views)

## Overview

The book attempts to answer the question:

> How do you document an architecture so that others can successfully use it, maintain it, and build a system from it?

### Why Document Software Architecture?

A good architecture is useless if people using it don't know what it is, can't understand it, or misunderstand it and apply it incorrectly.

It delivers value to developers, deployers, testers, and clients.

- **Education**. New team members, third party developers, or product owners.
- **Communication**. Explaining how a feature is implemented or discussing an approach for a new feature.
- **Analysis**. What needs to be tested when modifying or adding code. Risk analysis when modifing or adding code. Ensures features are implemented in accordance with the system's quality attributes.

### Quality Attributes

Quality attributes such as performance, reliability, security, and modifiability are important. Architecture is where these concerns are addressed.

Different quality attributes require different attention. For example:

- **Performance**. Exploit parallelism
- **Security**. Identify where unauthorised intrusion will do the most damage
- **Modifiability**. Separate concerns so changes are isolated

## Architecture Views

Views are the core concept associated with architecture documentation.

> Documenting an architecture is a matter of documenting the relevant views then adding documentation that applies to more than one view.

A documentation package can be composed of one or more views and documentation explaining how the views relate to one another.

Different views expose different quality attributes and support different goals. For example a *layered view* tells you about portability, a *deployment view* lets you reason about performance and reliability.

The documentation for a view contains:

- Primary presentation, usually graphical, showing primary elements and relations.
- An element catalog (key) that defines the presented elements.
- Specification of the elements' interfaces and behaviour.
- Rationale and design information.

The documentation that applies to *all of the views* contains:

- Introduction to the entire package.
- Constraints and rationale for the overall architecture.
- Management information required to maintain the package.

## Architecture Styles

When you apply a style to a system, the result is a view.

There is no fixed set of views that is appropriate for every system. There are some broad guidelines which can help:

- How the software is structured as a set of implementation units.
- How the software is structured as a set of elements that have runtime behaviour and interactions.
- How the software relates to non-software structures in its environment.

The are three categories of styles in the book:

- Module styles
- Component-and-connector styles
- Allocation styles

## Module Views

Module views document a system's principal units and the way they are decomposed to make the system.

Module views are used for:

- **Construction**. Provide a blueprint for source code.
- **Analysis**. Requirements traceability and impact analysis.
- **Communication**. Explain the system's functionality.

### Decomposition Style

The decomposition style is used for decomposing a system into units of implementation. A decomposition view describes the organisation of the code as modules and submodules and shows how system responsibilities are partitioned across them.

When to use a decomposition view:

- **Achieve quality attributes**. For example to support modifiability, to encapsulate changing parts of the system in modules, so the impact of change is localised.
- **Build vs buy decisions**. Some modules may be available from third parties, or be available from previous projects. These modules already have a set of responsibilities implemented, the remaining responsibilities can then be decomposed around the established modules.
- **Product line implementation**. To distinguish common modules, used in most products and modules.
- **Team allocation**. To allow implementation of different responsibilities in parallel.

Also useful for reasoning about and communicating the structure of software.

### Uses Style

A module *uses* another module if its correctness depends on the correctness of the other.

The uses styles goes a step further than the decomposition style. It reveals which modules use other modules.

The uses style is useful for:

- Planning incremental development
- Debugging and testing
- Risk analysis and change impact

### Generalisation Style

### Layered Style

### Aspects Style

### Data Model Style

## Component-and-connector Views

Component-and-connector (C&C) views document the system's units of execution.

## Allocation Styles Views

Allocation views document the relations between the system's software and non-software resources of the development and execution environment.
