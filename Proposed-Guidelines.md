![OCP Logo](./images/OCP-logo.png)

# Proposed Guidelines for OCP Specifications

Revision: 

Date:

---

# Revision Table
| **Date** | **Revision** | **Author** | **Notes** |
| :---     | :---         | :---       | :---      |
| WIP      | WIP          | Russ Wunderlich (OCP) | WIP - |
|          |              |            |           | 

---

# Goal
The goal of this document is to provide the framework for OCP Specification contributions. 

This is a working version presenting an initial, evolving framework intended to establish alignment and guide future refinements.

# Scope
The framework will establish a common approach by aligning expectations, providing guidelines, and offering instructions for creating specification contributions.

- Expectations: Define what is required from contributors to meet specification standards.
- Guidelines: Outline the recommended structure and content for specifications.
- Instructions: Detail how to use the provided template to create and submit your specification.

# Table of Contents
  - [Revision Table](#revision-table)
  - [Goal](#goal)
  - [Scope](#scope)
  - [Specification Usage and Types](#specification-usage-and-types)
  - [Guidelines](#guidelines)
    - [Vendor Information](##vendor-information)
    - [Citations](#citations)
    - [Revisions](#revisions)
    - [Normative Language](#normative-language)
  - [Specification Formatting and content](#specification-formatting-and-content)
  - [Project Review Guidelines and Checklist](project-review-guidelines-and-checklist)


# Specification Usage and Types
The scope of contributions within OCP is broad, ranging from silicon to systems, and from individual systems to complete data centers.
To enable specifications across this wide span, we start with high-level constructs and incorporate significant flexibility to accommodate diverse needs.

## Usages
For any framework to succeed, it must be grounded in a clear understanding of use cases. To guide the framework definition, three primary usage categories are identified:

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
The Base Specification is an architectural framework for coarse alignment providing requirements for flexible hardware and software modules/layers to interoperate. Market requirements drive Base Specifications. Without defining details of a specific design, the Base Specification may be light on IP content. This structure enables and simplifies the process for multiple parties (including potential competitors) to engage in this phase.

This layer defines the technical details for one of the following:
- Conceptual framework for an extensible technology platform/layer, representing technical community wide consensus and possibly used as a de-facto standard
- Requirements for a specific solution
- Extension/modification of an existing specification 

### Design
The design layer goes deeper than the architectural specification by detailing how the system will be implemented at the component and module level.

The Design Specifications has detail that further defines what specific role this contribution plays, and enough detailed design information such as high level board layouts etc that enables end users to begin the journey to realize this in the market. One or more parties may join to develop detailed design specs. Compared to the Base Specification, this effort typically contains significantly more detail such as future roadmaps and IP-related information. 

Design Specifications can be reused! I.e., if one contributor uses an indoor design specification, another team could reuse and make an outdoor specification. Having the same Base Specification for several Design Specifications will help increase the commonality of physical and logical interfaces to meet a set of common infrastructure hw/sw/fw requirements while allowing gen-to-gen variations or product differentiation.

This document defines the technical details for one of the following types of specifications:
- Design Specification for an intended physical hardware product type
- modification of an existing specification (state which existing spec is being modified)
- a specification with additional detail over the Base Specification for a product type.


### Product
The product layer is an implementation-level specification providing the exacting details of the end-product. 

The Product Specification captures manufacturing requirements including all design and build files, building on the Design Specification. 

Product Specifications can be reused! I.e., assuming the base and design specifications allow, if one contributor creates a 110VAC design specification, another team could reuse and make an -48VDC product specification.

This document defines the technical details for one of the following types of specifications:
- Product Specification for an intended physical hardware product type
- modification of an existing product specification
- a detailed specification for a product type

# Guidelines
## Vendor Information

1. **Neutral Treatment of Vendors**  
Vendors must not be promoted or demoted in any documentation, communication, or system configuration.
2. **Component References**  
Specific vendor components should not be explicitly named. When necessary, use generic phrasing such as “a component like XYZ” or entertain enabling a component specification that does not favor a particular vendor.

## Citations
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



## Revisions
As part of establishing the framework, we need to align on revision levels. While many organizations adopt a highly structured approach to version and revisioning, this rigor does not appear necessary for OCP.  Instead we propose a simplified progression:  

0.3 = initial version containing sufficient content (e.g., TOC, vision, scope ...) to enable alignment
0.5 = majority of content defined,  with some areas requiring additional detail
0.8 = definition complete and implementable, though not fully reviewed
1.0 = reviewed and implementable across all capabilities
1.x = use dot revisions for minor changes. Prefer increments of tenths (e.g., r1.1); use hundredths (e.g., r1.05) if many revisions are anticipated
2.x = use whole number revisions for major changes. There is no implication of forward or backward compatibility.

- Additional revisions between the designated milestones are allowed but generally discouraged. 
- Versioning is not required. If desired, versioning can be included in the specification name (i.e., Recliner V1 r1.0, Recliner V2 r0.5). 

## Normative Language
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

- [ ] is the specification type declared (base, design, product)?
- [ ] is the revision consistent with revision guidelines?
- [ ] does it have ToC, ToF, ToT? 
- [ ] is the revision table complete and of sufficient detail to be useful?
- [ ] Is normative language present and properly utilized?
- [ ] Is there a compliance table of sufficient detail to be usable?
- [ ] Are there any specifications referenced which are not released/published specifications?
- [ ]  


