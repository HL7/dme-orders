[Previous Page - Security and Privacy](security_and_privacy.html)

# FHIR RESTful communication pattern 

**Assumptions (without an Intermediary)**

1. The Supplier has restful query capabilities.
2. The Supplier can manage subscriptions on a specific Task resource.
3. The Supplier can authenticate to and is authorized to query the EHR.

**Flow Diagram (without an Intermediary)**

The flow diagram has three parts. 

1. Creation of the order.
2. Order updates by the Rendering Provider, which covers any changes to the status of the order, up to and including the fulfilment of the order.
3. Order updates by the Ordering Provider (e.g. order change or cancel).

<table><tr><td><img src="PAOREST.jpg" /></td></tr></table>


**Assumptions (with an Intermediary)**

1.	The Intermediary is the owner and “home” of all Task resources for this workflow.
2.	The Intermediary can manage subscriptions on a specific Task resource, and generally on Task resources.
3.	The Rendering Provider has restful query capabilities
4.	The Rendering Provider has a longstanding subscription for Task resources where they are the Task performer.
5.	The Intermediary has established authorization and authentication relationships with both the Ordering Provider and the Rendering Provider
6.	The intermediary will either use URL-rewriting for all references and links pointing to the Ordering Provider or Rendering Provider, or it creates copies of the resources local to the Intermediary to enable RESTful retrieval without direct Ordering Provider / Rendering Provider interaction

**Flow Diagram (with an intermediary)**

The flow diagram has three parts. 

1. Creation of the order. (Note: In this case it is useful to have an indication that the Rendering Provider is actually aware of the order, so this extra step is added in the first part.)
2. Order updates by the Rendering Provider, which covers any changes to the status of the order, up to and including the fulfilment of the order.
3. Order updates by the Ordering Provider (e.g. order change or cancel).


<table><tr><td><img src="PAORESTINT.jpg" /></td></tr></table>

[Next Page - FHIR Messaging exchanges](fhir_messaging_exchanges.html)