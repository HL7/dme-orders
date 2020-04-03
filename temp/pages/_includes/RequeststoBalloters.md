[Previous Page - Must Support and Missing Data](MustSupportandMissingData.html)

# Requests to balloters 

A) We are soliciting input on the exact methods we should use for communicating order updates and cancels
1. via a message bundle with the same content (in general) as the original message
2. via an update to the Task that includes an updated order resource (what about any additional documentation requirements)
3. via some other method 

B) We are soliciting input on the scope of examples necessary to assist the implementer community

C) We are soliciting input on the use of the Subscription resource on the Task resource as a way of communicating updates by the service provider to the ordering provider. While we may recommend the use of a notification with a subsequent request for the current status by the ordering provider, we have made provision for the subscription to request a complete response including the Task and the specific order resource.

D) We request feedback on the specific profiles in this version of the IG.  In particular, please comment on the cardinality constraints and the use of Must Support.

E) Since we plan to add a number of PAO specific value sets in the STU version, please only comment on specific value sets to the extent you have firm recommendations

F) Please comment on the applicability of this IG to all post-acute orders (not just orders for DME and Home Health)

G) The current extension are planned to allow for the specification of
1. order detail for the ServiceRequest
2. relevant reviews for all of the order profiles (DeviceRequest, ServiceRequest, MedicationRequest) that may include items such as prior authorization, documentation review, appropriate use reviews.
 
     Please comment on the need for other specific extension to support the process of ordering post-acute services and devices

