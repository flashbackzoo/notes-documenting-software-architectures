# Documenting Software Architectures

Notes on the book [Documenting Software Architectures: Views and Beyond](http://resources.sei.cmu.edu/library/asset-view.cfm?assetID=30386).

## Contents

- [Overview](#overview)
    - [Why Document Software Architecture?](#why-document-software-architecture)
    - [Quality Attributes](#quality-attributes)

## Overview

The book attempts to answer the question:

> How do you document an architecture so that others can successfully use it, maintain it, and build a system from it?

### Why Document Software Architecture?

A good architecture is useless if people using it don't know what it is, can't understand it, or misunderstand it and apply it incorrectly. This means the time spent designing it has been wasted.

It delivers value to developers, deployers, testers, and clients.

- Education: New team members, third party developers, or product owners.
- Communication: Explaining how a feature is implemented or discussing an approach for a new feature.
- Analysis: Provides a view of what needs to be tested when modifying or adding new code. Ensures features are implemented in accordance with the system's quality attributes. 

### Quality Attributes

Quality attributes such as performance, reliability, security, and modifiability are important in almost all systems.

Architecture is where these concerns are addressed.

Different quality attributes require different attention. For example:

- Performance: Exploit parallelism
- Security: Identify where unauthorised intrusion will do the most damage
- Modifiability: Separate concerns so changes are isolated

