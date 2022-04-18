# FHIR Messaging communication pattern

**Assumptions (without an Intermediary)**

1.	There is no RESTful access to the information in the EHR, or, all the information needs to be present in a single unit.
2.	Any additional information needed by the supplier may be available via RESTful queries from the EHR.
3.	The MessageDefinition resource for each message is available as a static artifact to be used as a reference, but it is not present in the message itself.
4.	The structure of each message is as follows:

			a.	A Bundle where the MessageHeader resource is the first entry.
			b.	MessageHeader.focus references the Task resource in the MessageBundle
			c.	The resources of all other entries in the Bundle are reachable from the MessageHeader resource (through Task or directly), and any references to resources that are not in the Bundle are logical references (via identifiers, not URLs).
 

**Flow Diagram (without an Intermediary)**

The flow diagram again has three parts. Each message is shown with a synchronous response, that comes from the $process-message endpoint of the receiver.

Note that any messages from the Rendering Provider to the Ordering Provider could be presented as an asynchronous message response (similar to the application-level acknowledgements in HL7 v2 messages) using the MessageHeader.response structure. However, since the implementation guide explicitly calls out the use of intermediaries, keeping track of the correct MessageHeader.response.identifier value would be an additional requirement for them that is not necessary - the use of Task allows responses to be linked with the original order without MessageHeader.response.

1. The first part shows the sending of the order. A successful synchronous response indicates that the order has been received.
2. The second part represents order updates by the Rendering Provider, which covers any changes to the status of the order, up to and including the fulfillment of the order.
3. The third part shows order updates by the Ordering Provider (e.g. order change or cancel).

<table><tr><td><img src="PAOMsg.jpg" /></td></tr></table>


**Assumptions (with an Intermediary)**

1.	There is no RESTful access to the information in the Ordering Provider System, or, all the information needs to be present in a single unit.
2.	Any additional information needed by the Rendering Provider needs to be exchanged via order update messages, since one of the main purposes of the Intermediary is to proxy the access between the Ordering Provider and the Rendering Provider.
3.	MessageHeader.response is not used for the order update messages.
4.	The MessageDefinition resource for each message is available as a static artifact to be used as a reference, but it is not present in the message itself.
5.	The structure of each message is as follows:

			a.	A Bundle where the MessageHeader resource is the first entry.
			b.	MessageHeader.focus references the Task resource in the MessageBundle
			c.	The resources of all other entries in the Bundle are reachable from the MessageHeader resource (through Task or directly), and any references to resources that are not in the Bundle are logical references (via identifiers, not URLs).
 

**Flow Diagram (with an Intermediary)**

The flow diagram again has three parts. Each message is shown with a synchronous response, that comes from the $process-message endpoint of the receiver.

Note that any messages from the Rendering Provider to the Ordering Provider could be presented as an asynchronous message response (similar to the application-level acknowledgements in HL7 v2 messages) using the MessageHeader.response structure. However, since the implementation guide explicitly calls out the use of intermediaries, keeping track of the correct MessageHeader.response.identifier value would be an additional requirement for them that is not necessary - the use of Task allows responses to be linked with the original order without MessageHeader.response.

1. The first part shows the sending of the order. A successful synchronous response indicates that the order has been received.
2. The second part represents order updates by the Rendering​ Provider, which covers any changes to the status of the order, up to and including the fulfillment of the order.
3. The third part shows order updates by the Ordering Provider (e.g. order change or cancel).

<table><tr><td><img src="PAOMsgInt.jpg" /></td></tr></table>