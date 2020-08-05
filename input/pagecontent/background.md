[Previous Page - Index](index.html)

# Current environment
There is currently no commonly accepted method of defining and exchanging post-acute orders between ordering providers and the providers of the ordered services or devices (rendering providers).  This guide defines a framework for ordering any type of post-acute services and provides for the inclusion of appropriate documentation to support 1) the medical necessity of the orders, 2) refining the order based on clinical information, and 3) communicating specific reviews or approvals to support appropriate billing.  This exchange:
1.	Speeds the ordering process and delivers needed care sooner.
2.	Provides a method for electronic exchange to automate acceptance or rejection of the order.
3.	Supports exchange of required documentation.
4.	Supports exchange of information related to order review/approval (e.g. Prior Authorization, Appropriate Use, Order and Documentation Review). However, the use of this IG is primarily to communicate the specific post-acute service order and is not dependent on any review/approval process.

The goal is to provide for electronic ordering of Post-Acute DME and Home Health Services with the electronic exchange of supporting documentation in this version of the IG.  It is the goal of future versions of this implementation guide to support orders for all post-acute services.

**In Scope**
1.	Durable Medical Equipment (DME) and associated supplies using DeviceRequest.
2.	Medications associated with DME items such as nebulizers and infusion pumps using MedicationRequest.
3.	Home Health Services covered by a home health plan of care using ServiceRequest
4.	Extension to exchange Prior-Authorization, Appropriate Use, Medical Review information  for DeviceRequest, ServiceRequest and MedicationRequest.
5. 	Extension for orderable item details for ServiceRequest.
6.	RESTful and Messaging based exchanges between the ordering and performing providers.
7.	Exchange for supporting documentation to support the specific order or provide the rendering provider with information necessary to meet payer requirements.

**Out-of-Scope**
1.	Responses from the patient 
2.	Patient directed care
3.	Services other than DME (including medications) and  Home Health Services
4.	Cost considerations
5.	Partial fulfillment: status is included, but the details (which may require a conversation between the ordering and rendering provider) are out of scope
6.	Documentation requests – if the performing provider needs additional documentation from the ordering provider that is not included in the exchanges defined in this IG, the authors suggest the use of the [Da Vinci Clinical Data Exchange (CDex) IG](http://build.fhir.org/ig/HL7/davinci-ecdx/index.html) which support clinical data exchange between provider as well as between a provider and a payer.
7.	This IG does not require the use of a digital signature for this version, but the optional use of provenance to support digital signatures in scope

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
2.  the underlying FHIR standards for the associated release (e.g. [FHIR R4](http://hl7.org/fhir/)), and 
3. [US Core R4](http://build.fhir.org/ig/HL7/US-Core-R4/) profiles as applicable.

Note: Other standards are available or in process to communicate referral information between providers such as the [Bidirectional Services eReferrals (BSeR)](http://hl7.org/fhir/us/bser/2019May/BSeRMessagingWorkflow.html) that are patterned after the 360x referral process. The PAO IG is focused on a simple method to exchange and track post-acute orders and the supporting documentation. PAO supports both a messaging and RESTful method for exchanging and tracking post-acute care orders including orders for services not covered by BSeR such as DME.  In the future, we will harmonize the statuses defined in this guide with the state machine work in BSeR.


[Next Page - Security and Privacy](security_and_privacy.html)