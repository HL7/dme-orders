[Previous Page - FHIR Messaging exchanges](fhir_messaging_exchanges.html)

# Mixed communication pattern

One of the purposes of an Intermediary can be to transition between different communication patterns, although this assumes a detailed understanding of the content, and requires the Intermediary to manage resources locally. 

This example shows using the RESTful pattern for the Ordering Provider, and messaging with the Rendering Provider.

1. The first part of creating the order includes the Intermediary getting all necessary resources from the Ordering Provider to package them as a message which is sent to the Rendering Provider. A successful message to the Rendering Provider is then reflected as a status of “received” in the Task resource, and the Ordering Provider is notified of the update.
2. The second part, updates/responses to the order from the Rendering Provider, starts with a message sent to the Intermediary, where all resources are stored and exposed locally, so the Ordering Provider can retrieve them after getting the updated Task.
3. The third part is for order updates from the Ordering Provider to the Rendering Provider, and the flow is similar to the new order part.


<table><tr><td><img src="PAOMixedInt.jpg" /></td></tr></table>

[Next Page - Technical Background](technical_background.html)