[Previous Page - Index](index.html)

# Current environment
There is currently no commonly accepted method of defining and exchanging post-acute orders between ordering providers and the providers of the ordered services or devices (rendering providers).  This guide defines a framework for ordering any type of post-acute services and provides for the inclusion of appropriate documentation to support 1) the medical necessity of the orders, 2) refining the order based on clinical information, and 3) communicating specific reviews or approvals to support appropriate billing.  This exchange:ppropriate billing.
1.	Speeds the ordering process and delivers needed care sooner.
2.	Provides a method for electronic exchange to automate acceptance or rejection of the order.
3.	Supports exchange of required documentation.
4.	Supports exchange of information related to order review/approval (e.g. Prior Authorization, Appropriate Use, Order and Documentation Review).

The goal is to provide for electronic ordering of DME and Home Health Services with the electronic exchange of supporting documentation.

**In Scope**
1.	DME that does not have special resource needs
2.	Home Health that does not have special resource needs (e.g. medication administration)
3.	Task , Subscription for workflow
4.	Extension to describe Prior-Authorization, Appropriate Use, Medical Review information
5.	Guidance on Authentication and Authorization
6.	Create status value set
7.	Orderable items
a.	Home health - items covered by care plan with exceptions mentioned above
b.	DME - any valid HCPCS with exceptions mentioned above

**Out-of-Scope**
1.	Responses from the patient 
2.	Patient directed care
3.	Non-DME / Home Health
4.	Cost considerations
5.	Partial fulfillment status is included, but the details are out of scope
6.	Additional Documentation request – this is part of the Clinical Data Exchange (CDex) IG http://build.fhir.org/ig/HL7/davinci-ecdx/index.html
7.	Requirement for a Digital Signature is out of scope for this version, but the optional use of provenance to support them is in scope

**Business Requirements**
The goal of this implementation guide is to provide a framework in which ordering providers can exchange orders and documentation with rendering providers to:
1.	Communicate clinical orders electronically for DME and Home Health
2.	Communicate documentation to perfect the order and/or establish medical necessity
3.	Handling updates, cancellation, and rejection of the order with/by the rendering provider

**Clinical Requirements**
Clinical requirements to support this implementation guide include the following items.
1.	Determining the appropriate ordered service and/or device.
2.	Completing documentation to support the medical necessity of the ordered service or device.
3.	Performing any required actions by the ordering provider to authorize (prior authorization), determine appropriateness (appropriate use), establish completeness of the documentation (documentation review) and communicate it to the rendering provider.
4.	Identifying the rendering  provider or intermediary to receive the order and supporting documentation.

**Testing Requirements**
This IG has been constructed in a manner that allows testing of conformance to:
1. the profiles defined in this guide, 
2.  the underlying FHIR standards for the associated release (e.g. FHIR R4), and 
3. US Core R4 profiles as applicable.


[Next Page - Workflow](workflow.html)