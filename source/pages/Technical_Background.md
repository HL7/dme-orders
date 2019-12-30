---
title: Technical Background
layout: default
active: Technical Background
---

[Previous Page](Background.html)

# Systems
The PCDE implementation guide defines the responsibilities of the three types of systems involved in a Post-Acute Orders solution:
* **Ordering Provider systems**  Systems that manage data on behalf of a payer who is a source for data to be transferred
* **Performing Provider / Supplier systems**  Systems that manage data on behalf of a payer who is an intended recipient of transferred data.
* **Intermediary Systems** Systems that communicate with both the Ordering Provider Systems and the Performing Provider / Suppler Systems and provide appropriate supplier determination (in some cases in conjunction with the patient and or payer), translation services and, where necessary, order detail routing and integration.

# Underlying technologies
This guide is based on the HL7 FHIR standard. Implementers of this specification therefore need to understand some basic information about these specifications.

**FHIR**

This implementation guide uses terminology, notations and design principles that are specific to FHIR. Before reading this implementation guide, its important to be familiar with some of the basic principles of FHIR as well as general guidance on how to read FHIR specifications. Readers who are unfamiliar with FHIR are encouraged to read (or at least skim) the following prior to reading the rest of this implementation guide.
* 	FHIR overview
* 	Developers introduction (or Clinical introduction)
* 	FHIR data types
* 	Using codes
* 	References between resources
* 	How to read resource & profile definitions
* 	Base resource

This implementation guide supports the R4 version of the FHIR standard. R4 is just recently published and the goal is to ensure the implementation guide is aligned with the current direction of the FHIR standard.
Because of this IGs focus on workflow issues between an ordering provider and the performing provide / supplier implementers should also familiarize themselves with the following FHRI resources and operations.
* 	MessageHeader
* 	MessageDefinition
* 	Task
* 	Subscription
* 	ProcessMessage


[Next Page](FHIR_Artifacts.html)