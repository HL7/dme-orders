[Previous Page - FHIR Artifacts Overview](fhir_artifacts_overview.html)

# Must Support and Missing Data

Systems claiming to conform to a profile SHALL support the elements in a profile as defined below: This guide adopts the following definitions of MustSupport for all direct transactions between the Sender and Recipient or Intermediary

**All Sending Systems**

Sending Systems are defined as: 1) Ordering Provider Systems and 2) Intermediary Systems when sending to a Rendering Provider Systems using the PAO IG
* As part of the PAO transaction as specified by the PAO IG, 
the Sender SHALL be capable of including all elements defined in the PAO profiles that have a MustSupport flag.
 	SHALL populate all elements with a MustSupport flag if the information exists
* In situations where information on a particular data element is not present, the Sender SHALL NOT include the data elements in the resource instance as part of a $process-message operation or a query response if the cardinality is 0..n
* If the information does not exist and the cardinality of the element is >= 1..*, the Sender SHALL send the reason for the missing information using values from the value set indicating the absent reason or use the dataAbsentReason extension where it is defined. 
Note: populating the element with the value set absent reason or using the dataAbsent Reason should be handled by the Sending System and not require provider action. 

**All Receiving Systems** 

Receiving Systems are defined as 1) Rendering Provider Systems and 2) Intermediary Systems when receiving from the Ordering Provider Systems using the PAO IG.
* The Recipient/Intermediary SHALL be capable of processing resource instances containing the data elements without generating an error or causing the application to fail. 
* Recipient/Intermediary Systems SHOULD be capable of processing (display, store, etc) the data elements based on the utility of the specific element to the rendering provider and the specific item or service being ordered.
* When receiving a PAO Order from the Sender, the Recipient/Intermediary SHALL interpret missing data elements within resource instances as data not present in the Senders systems.
* PAO Order Recipient/Intermediary Systems SHALL be able to process resource instances containing data elements asserting missing information without generating an error or causing the application to fail.

**Conformance to US Core Profile** 

Where this IG does not additionally constrain a US Core profile, the actors shall follow the US Core definition of [Must Support and Missing Data](http://hl7.org/fhir/us/core/general-guidance.html)
