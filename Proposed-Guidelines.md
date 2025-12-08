![OCP Logo](./images/OCP-logo.png)

# Proposed Guidelines for OCP Specifications


# Goal
The goal of this document is to provide the framework for OCP SPecification contributions.

This version (track commits) presents an initial, evolving framework intended to establish alignment and guide future refinements.

# Scope
The framework will establish a common approach by aligning expectations, providing guidelines, and offering instructions for creating specification contributions.

- Expectations: Define what is required from contributors to meet specification standards.
- Guidelines: Outline the recommended structure and content for specifications.
- Instructions: Detail how to use the provided template to create and submit your specification.

# Table of Contents
  - [Goal](#goal)
  - [Scope](#scope)
  - [Revision Table](#revision-table)
  - [Specification Usage and Types](#specification-usage-and-types)
  - [Vendor Information](#vendor-information)
  - [Citations](#citations)
  - [Revisions](#revisions)
  - [Normative Language](#normative-language)
  - [Compliance](#compliance)
  - [Specification Formatting and content](#specification-formatting-and-content)
  - [Project Review Guidelines and Checklist](project-review-guidelines-and-checklist)

# Revision Table
Create one

# Specification Usage and Types
The scope of contributions within OCP is broad, ranging from silicon to systems, and from individual systems to complete data centers.
To enable specifications across this wide span, we start with high-level constructs and incorporate significant flexibility to accommodate diverse needs.

## Usages
For any framework to succeed, it must be grounded in a clear understanding of use cases. To guide the framework definition, three primary usage categories are proposed:

1. Introduce a new technology/direction to the community
- Rapid decision making enabling quick release of a contribution
- initial revision is typically sufficient for narrow, specific implementation
- may require additional community work to address broader needs 

2. Enabling a full ecosystem
- builds on an existing baseline (any source), to evolve or define a specification for the broader ecosystem
- expanded use cases and thorough vetting equates to a slower process
- typically has stepping-stone approach, adding use cases with each revision 

3. Technology development/evolution
- planned technology development requiring strong community engagement 
- expects spec progression through multiple revisions (0.3, 0.5, 0.8, 1.0) to achieve final, implementable results
- represents the slowest progression and highest detail level

These three usage categories apply across all levels, from architecture to implementation, and any contribution may align with each category throughout its revisions. When evaluating the framework, key considerations include:
- depth of detail: Comprehensive specification details vs. “Good enough” specification
- Industry alignment: many specification are tightly aligned to industry standards and may need additional considerations
- Flexibility for innovation: Allowance for exploration w/o having a predefined roadmap

## Types
The three types or layers of OCP specifications are Base, Design, and Product.

![Layers](./images/layers.png)

Any or all of the layers could be utilized for any particular contribution. 
Examples:
- A base layer defines the architecture and requirements for a nuclear power source for an AI Datacenter. The subsequent design specification details how to meet the base requirements with specific design elements and more detailed requirements for a Molten Salt Reactor (MSR). The final specification, the product spec, provides the implementation details (and potentially manufacturing files) for the "MSRv5 Power Module", a fifth generation MSR from the Nuclear Are Us store. 
- The Nuclear Are Us store provides (only) a design specification in order to create a larger supplier base for the MSR.

### Base
The base is an architectural-level specification which defines the high-level structure and organization of a "system", focusing on components, their interactions, and the principles guiding design.

Its scope typically includes:
1. A vision
- Purpose and objectives of the system
- High-level description of functionality
- enumerated Requirements


2. Architectural Principles

Design philosophies (e.g., modularity, scalability, security).
Standards and guidelines (e.g., coding standards, interoperability).


3. System Components

Identification of major components or modules.
Responsibilities and roles of each component.
Interfaces between components.


4. Data Architecture

Data flow across components.
Storage and retrieval mechanisms.
Data models and schemas (at a conceptual level).


5. Interaction and Communication

Communication protocols.
Integration points with external systems.
API specifications (high-level).


6. Non-Functional Requirements

Performance, scalability, reliability.
Security and compliance considerations.
Maintainability and extensibility.


7. Deployment and Environment

Target platforms (cloud, on-premises, hybrid).
Hardware/software requirements.
Network topology.


8. Risks and Assumptions

Known limitations.
Dependencies on third-party systems.
Assumptions about future growth or technology.


9. Architectural Views

Logical View: Functional decomposition.
Physical View: Deployment diagram.
Process View: Concurrency and synchronization.
Development View: Code organization and build process.

### Design
The design layer goes deeper than the architectural specification by detailing how the system will be implemented at the component and module level.

Its scope typically includes:

1. Detailed Component Design

Internal structure of each component/module.
Class diagrams, object models, and relationships.
Responsibilities and interactions within modules.


2. Data Design

Detailed data structures (tables, classes, attributes).
Database schema with keys, constraints, and indexes.
Data validation rules and transformation logic.


3. Interface Design

Precise API definitions (methods, parameters, return types).
User interface layouts and navigation flows.
Communication protocols and message formats.


4. Algorithm and Logic Specification

Detailed algorithms for core functionalities.
Pseudocode or flowcharts for complex processes.
Error handling and exception management.


5. State and Behavior Modeling

State diagrams for dynamic components.
Sequence diagrams for interactions.
Activity diagrams for workflows.


6. Non-Functional Details

Performance tuning strategies.
Security mechanisms (encryption, authentication).
Resource utilization and optimization.


7. Integration Details

How modules integrate and interact.
Dependency management.
Versioning and compatibility considerations.


8. Testing and Validation Hooks

Unit test specifications.
Mock interfaces for integration testing.
Acceptance criteria for each module.


9. Deployment-Level Details

Configuration files and environment variables.
Build scripts and packaging instructions.
Continuous integration/continuous deployment (CI/CD) setup.

### Product
The product layer is an implementation-level specification providing the exacting details of the end-product. 

Its scope typically includes:

1. Code-Level Details

Programming language(s) and frameworks.
Detailed class definitions, methods, and attributes.
Inline documentation and coding standards.


2. Configuration and Environment Setup

Development, staging, and production environment specifications.
Configuration files, environment variables, and secrets management.
Dependency management (libraries, packages, versions).


3. Database Implementation

Complete schema with tables, indexes, triggers.
Stored procedures and queries.
Migration scripts and versioning.


4. API and Service Implementation

Full endpoint definitions with request/response formats.
Authentication and authorization mechanisms.
Error codes and handling strategies.


5. Build and Deployment Instructions

Build scripts and automation tools.
CI/CD pipeline configuration.
Containerization (Docker) and orchestration (Kubernetes) details.


6. Integration Details

How external services are connected (SDKs, APIs).
Data exchange formats (JSON, XML).
Version compatibility and backward support.


7. Testing Implementation

Unit, integration, and system test scripts.
Test data and mock services.
Code coverage and quality metrics.


8. Performance and Optimization

Profiling and tuning strategies.
Resource allocation (CPU, memory).
Caching and load balancing configurations.


9. Security Implementation

Encryption methods for data at rest and in transit.
Secure coding practices.
Vulnerability scanning and patching.


10. Maintenance and Support

Logging and monitoring setup.
Error reporting and alerting.
Upgrade and rollback procedures.

# Vendor Information

1. **Neutral Treatment of Vendors**  
Vendors must not be promoted or demoted in any documentation, communication, or system configuration.
2. **Component References**  
Specific vendor components should not be explicitly named. When necessary, use generic phrasing such as “a component like XYZ” or entertain enabling a component specification that does not favor a particular vendor.

# Citations
ing specifications that have not yet been published

## Use of Non-OCP Document Information
**General Principle**  
All specifications must include only materials for which the organization holds the necessary usage rights or that are legally available for free and unrestricted use.

**Best Practices**
* Prefer Referencing Over Incorporation 
Whenever possible, reference external material rather than embedding it directly in the specification. 
* Avoid Version Lock-In 
Referencing helps prevent binding the specification to a specific version unless absolutely required. 

**When Inclusion Is Necessary** 
* Use Original Wording 
Describe the information in your own words whenever possible. 
* If Direct Inclusion Is Required 
Clearly state the source of the material. 
Ensure all legal and usage requirements are met (e.g., copyright notices, required attribution). 

**Permitted Sources**  
Examples of allowed sources include:
* Apache 
* OIF 
* MIL-SPEC 


## Modification of non-OCP industry standards

how is it we produce unique specification requirements then rely on group.io to address?  very hit or miss



# Revisions
0.3
0.5
0.8
1.0

# Normative Language
Normative language establishes clear, enforceable requirements and removes ambiguity. Requirements are the basis for compliance.

- Shall = requirement
Requirements are mandatory, must be done
Including the word “not” (as in shall not) specifies a mandatory prohibition, meaning the requirement explicitly forbids the action.

- Should = recommendation
Recommendations are optional yet indicate a preferred direction if implemented
Including the word “not” (as in should not) indicates a strong recommendation against performing an action

- May = allowable
Indicates flexibility of choice (option) with no implied preference.

**All specifications shall utilize normative language.** 

# Compliance

# Specification Formatting and content

## Table of Contents

## Table of Figures

## Table of Tables

## Compliance

# Project Review Guidelines and Checklist
## Guidelines
Define a minimal process & checklist that each workstream executes prior to contribution hub submittal
Checklist submitted with contribution
Expectations
- Fully inclusive with defined minimum set of reviewers
- Invitations to dependent/adjacent workstreams
- All feedback tracked & dispositioned

Final form verified to requirements before uploading to contribution hub

## Checklist
note to self: need to pull this to a separate document, here for ease at this point

1. is the specification type declared (base, design, product)?
1. is the revision consistent with revision guidelines?
1. does it have ToC, ToF, ToT? 
1. is the revision table complete and of sufficient detail to be useful?
1. Is normative language present and properly utilized?
1. Is there a compliance table of sufficient detail to be usable?
1. Are there any specifications referenced which are not released/published specifications?
1. 


