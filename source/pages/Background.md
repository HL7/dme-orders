---
title: Background
layout: default
active: Background
---

[Previous Page](Post-Acute_Orders_Home.html)

# Current environment
Patients that move from one payer to another frequently experience interruptions or delays to existing care for chronic and acute conditions related to the inability of the new payer to obtain information about the ongoing treatment, understand its progress and verify the clinical need for such treatments. This frequently requires the patient or providers to change therapies, tolerate delays in care, see additional providers or schedule additional visits, and fill out or resubmit additional documentation showing that the care is medically necessary and appropriate. The process creates a significant burden on providers, add unnecessary costs, and introduces risk to the patient.

There is currently no commonly accepted method of defining and exchanging post acute orders between ordering providers and the suppliers of the ordered services or devices.  This guide defines a framework for ordering any type of post acute services and provides for the inclusion of appropriate documentation to support the medical necessity of the orders to facilitate documentation for the purpose of refining the order and supporting appropriate billing .
1.	Speeds the ordering process and delivers need care sooner
2.	Provides for electronic exchange to automate acceptance or rejection of the order
3.	Support exchange of required documentation
4.	Support exchange of information related to order review/approval (e.g. Prior Authorization, Appropriate Use, Order and documentation review)

The goal is to provide for electronic ordering of DME and Home Health Services with the electronic exchange of supporting documentation.

**In Scope**
1.	DME that does not have special resource needs
2.	HH that does not have special resource needs (e.g. medication administration)
3.	Task , Subscription for workflow
4.	Extension to describe PA, AU, MR
5.	Guidance on Authentication and Authorization
6.	Create status value set
7.	Orderable items
a.	Home health - items covered by care plan with above exception
b.	DME - any valid HCPCS with above exception

**Out-of-Scope**
1.	Responses from the patient 
2.	Patient directed care
3.	Non-DME / Home Health
4.	Cost considerations
5.	Partial fulfillment - status only detail is out of band for now
6.	Additional Documentation request (in scope using CDex)
7.	Digital Signature (may be out of scope for V1)
8.	Order detail for specific services (part of DRLS) such as those involving medications

**Business Requirements**
The goal of this implementation guide is to provide a framework in which ordering providers can exchange orders and documentation with preforming providers and suppliers to:
1.	Communicating clinical orders electronically for DME and Home Healt
2.	Communicating documentation to perfect the order and/or establish medical necessity
3.	Handling updates, cancels and rejection of the order with/by the performing provider / supplier

**Clinical Requirements**
Clinical requirements to support this implementation guide include the following:
1.	determining the appropriate ordered service and/or device
2.	completing documentation to support the medical necessity of the ordered service or device
3.	performing any required actions by the ordering provider to authorize (prior authorization), determine appropriateness (appropriate use), establish completeness of the documentation (documentation review) and communicating it to the performing provider/supplier
4.	Identifying the performing provider / supplier or intermediary to receive the order and supporting documentation

**Testing Requirements**
This IG has been constructed in a manner that allows testing and validation - specifically:
1.  adherence to profiles defined in this guide, and 
2.  testing of conformance to the underlying FHIR standards for the associated release (e.g. FHIR R4).

[Next Page](Workflow.html)