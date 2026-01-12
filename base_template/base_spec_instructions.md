<!-- The intent for this file is to have the necessary instructions for the base spec template. We may find this unnecessary and simply integrate into the template. -->

**Table of Contents for Instructions** 
- [Title Page](#title-page)
- [Revision History](#revision-history)
- [License](#license)	
   - [Open Web Foundation (OWF) CLA](#open-web-foundation-owf-cla)
   - [Acknowledgements](#acknowledgements)
- [Trademarks](#trademarks) 
- [Compliance with OCP Tenets](#compliance-with-ocp-tenets)
   - [Openness](#openness)
   - [Efficiency](#efficiency)
   - [Impact](#impact)
   - [Scale](#scale)
   - [Sustainability](#sustainability)
- [Introduction](#introduction)
   - [Purpose of the Document](#purpose-of-the-document)
   - [Scope](#scope)
   - [Audience](#audience)
   - [Conventions](#Conventions)
- [Overview](#overview)
   - [Description](#description)
   - [Goals, Vision, Objectives](#goals-vision-objectives)
   - [User Requirements/User Stories](#user-requirementsuser-stories)
   - [Solution Architecture](#solution-architecture)
- [Main Section A](#main-section-a)
- [Main Section B](#main-section-b)
- [Main Section C](#main-section-c)
- [Appendix](#appendix)
   - [Glossary](#glossary-and-abbreviations)
   - [References](#references)
   - [Requirement Summary](#requirement-summary)
   - [Appendix D](#appendix-d)

---

# Title Page
**This section is mandatory.**  
The title page shall have the specification name, the revision, the publication date, as well as the enumeration of authors.
 
# Table of Contents
**This section is mandatory.**  
The table of contents shall enumerate the primary and secondary sections of the specification.

# Table of Figures
**This section is mandatory.**  
The table of figures shall enumerate the figures within the main body of the specification.

# Table of Tables
**This section is mandatory.**  
The table of tables shall enumerate the tables within the main body of the specification.

# Revision History
**This section is mandatory.**  
Record revision, publish date, authors and the high level changes made for the revision.  
You may have an appendix with a more detailed change enumeration if you desire.

# License
**This section is mandatory.**  
The template language is fixed, the only action necessary is to enumerate the contributor Name(s) or Company name(s)

## Acknowledgements
**This section is mandatory.**  
List all companies or individuals who may have assisted you with the specification by providing feedback and suggestions but did not provide any IP.  
use "None" or "N/A" if not applicable.

# Trademarks
**This section is mandatory.**  
List all trademarks referenced in the specification.  
use "None" or "N/A" if not applicable.

# Compliance with OCP Tenets
**This section and all tenets are mandatory.**  
For each of the tenets, detail how your contribution aligns and supports the tenet.

<!-- should probably just delete the text re tenets and point to source file https://146a55aca6f00848c565-a7635525d40ac1c70300198708936b4e.ssl.cf1.rackcdn.com/images/bf648bb75091907147e76846cad590f402660d2e.pdf -->

## Openness
Openness is measured by the ability of third parties to build, modify, or personalize your contributed device, platform, or software. The OCP aims for completely open platforms that include all programmable devices, firmware, software, mechanical and electrical design elements, and any necessary external components or tools like software utilities. Contributors are highly encouraged to collaborate with other OCP Projects that may have complementary knowledge and expertise. Actively remove barriers to openness and demonstrate collaboration by sharing, seeking feedback, and accepting changes to designs and specifications. Ensure your contribution can be extended and enhanced by others.

## Efficiency
Your contribution should be more efficient than existing or prior generations. Efficiency can be demonstrated through reduced operational and capital expenses, improved performance, modularity, increased capacity, lower power or water consumption, better utilization, reduced size, or minimized code weight and latency in software. Clearly express efficiency gains with metrics valued by end-users when proposing your contribution.

## Impact
Your contribution should have a transformative impact on the industry by introducing new technology, accelerating time-to-market, or enabling technology through global supply chains. Impact is amplified when new technologies are made accessible to many customers worldwide. Examples include widely adopted specifications or more specifically, open security features that establish and verify product trust. Ensure your contribution creates meaningful positive impact within the OCP ecosystem.

## Scale
Design your contribution for easy implementation and deployment at any scale, with minimal intervention. Aim to create additive solutions where minimal usage or instances can be deployed and incrementally scaled as needed to effectively address the entire problem. Provide all necessary tools and supporting documentation, such as installation guides, initialization processes, configuration information, and details on obtaining service support. Include features like simple manual and automated maintenance, remote management, upgradability, and error reporting. Management tools should be open-sourced and/or made available to adopters.

## Sustainability
Your contribution must be sustainable, maximizing transparency of environmental impacts with the goal of continuous improvement. Focus on the responsible use of natural resources, fostering positive societal impacts, and minimizing environmental harm. This can be achieved through design decisions that promote circularity, efficient use of materials, power-saving features, and sustainability labeling. For software, consider optimizing code to reduce resource consumption and incorporating features that enable energy efficiency.


# Introduction
**This section and all sub-sections are mandatory.**  
no text necessary in this section, simply the header

## Purpose of the Document
Clearly state the reason for creating this document, explain what it aims to achieve. 

## Scope
Define the boundaries of the document. Specify what is included and what is explicitly excluded. This helps prevent misunderstandings about coverage. 

## Audience
Identify the intended readers and their roles. This could include architects, engineers, developers, project managers, etc.

## Conventions
This section lists the standard conventions used in this specification.  
Normative language is mandatory, no modifications are necessary to this text.
Add in other conventions utilized in the specification (numerical representation etc.)

# Overview
**This section is mandatory.**  
This section provides a high-level summary of the system or solution. It sets the context for the entire specification and explains what the solution is intended to achieve.

## Description
**This section is mandatory.**  
Provide a concise explanation of what the system or solution is, including its primary function and role within the larger ecosystem. Include the problems it addresses. Explain its utility within the Open Compute Project ecosystem.

## Goals, Vision, Objectives
**This section is mandatory.**
Define the long-term vision and goals for the system or solution. Outline measurable objectives that guide decisions. This helps consumers of the specification understand the problem being addressed and how the solution fits into the broader context.

## User Requirements/User Stories
**This section is optional.**  
Capture what end-users or stakeholders need from the system. This can be expressed as high-level requirements or user stories to ensure the architecture aligns with real-world needs.  
If end-user stories or requirements we not utilized in the definition, then this section need not be present and the Goals, Visions, Objectives section will suffice.

## Solution Architecture
**This section is optional.**  
Present the high-level design of the solution, including major components, their interactions, and how they fulfill the goals and requirements. This section often includes diagrams (e.g., system context, component diagrams).  
For fundamental architectural level specifications, this section should be present and would evolve with revision progression.

# Main Section A
The sections labeled “Main Sections” constitute the main body of the document and are intentionally generic, allowing the author(s) to adapt them to the specific needs of the project. These sections should define requirements across multiple domains and may be organized in a structure that best supports the specification’s objectives.  
Examples of sections within the main body:
- HW specification: may address domains such as performance, mechanical, electrical, thermal, manageability, security, reliability, and regulatory compliance.
- SW specification: May cover domains such as data architecture, interfaces & protocols, performance & scalability, security, maintainability, test & validation.
- Domain level base specification: Could incorporate any or all of the above examples customized to meet the requirements of the specific dmain.
 
# Main Section B
# Main Section C

# Appendix
no text necessary in this section, simply the header
## Glossary and Abbreviations
**This section is mandatory.**  
Enumerate all unique definitions and abbreviations utilized in the specification.

## References
**This section is mandatory.**  
Enumerate & cross-link references throughout the specification  
ToDo: examples

## Requirement Summary
**This section is mandatory if requirement language is utilized.**  
ToDo: need to define the specific style

## Appendix D
**This section is optional.**  
Use additional sub-sections for other detail which need to be captured