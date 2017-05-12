# About #






## Overview: Social Care Domain Message Specification ##
The Social Care Domain Message Specification (DMS) defines a number of messages to support the exchange of structured information between healthcare and social care organisations.

The DMS currently covers the following information flow:

- Transfers of care from hospital to social services for patients with care and support needs

The requirements for this information flow are defined in the regulations under the Care Act 2014. The Act describes a series of notices that must be sent from hospitals to adult social services to support the discharge of hospital patients who have care and support needs. The notices are defined as follows:

- Assessment Notice

This is used by the hospital to inform social services that an assessment of the patient's care and support needs is required. Where known, it includes an expected discharge date.

- Discharge Notice

Following the issue of an Assessment Notice, a Discharge Notice is sent by the hospital to social services to confirm the patient's proposed discharge date.

- Withdrawal Notice

This is used to withdraw a previously issued Assessment Notice and/or Discharge Notice. A Withdrawal Notice may be required to be issued for a number of reasons, for example because the patient's medical condition has changed or the patient is eligible for NHS Continuing Health Care.

NHS Digital has developed an Information Standard [SCCI2075] that defines the minimum data sets that must be used for Assessment, Discharge and Withdrawal Notices, based on the regulations under the Care Act 2014. The Information Standard also defines a generic Notice Receipt data set that must be used to send an acknowledgement of a received notice from social services to the originating hospital. The data sets in the Information Standard have been used as the basis for the messages defined in this DMS.

 

**The FHIR resources are bundled together to construct:**

-	Assessment Notice
-	Assessment Notice Accept Response
-	Assessment Notice Reject Response
-	Discharge Notice
-	Discharge Notice Accept Response
-	Discharge Notice Reject Response
-	Withdrawal Notice
-	Withdrawal Notice Accept Response
-	Withdrawal Notice Reject Response


**Further Information**

This FHIR Messaging specification is based on and intended to be used alongside the published [FHIR DSTU2 1.0.2] (October 2015) specification. 

[FHIR DSTU2 1.0.2]: http://hl7.org/fhir/DSTU2/index.html

[Work_Stream_2.1_Final.pdf]: https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/465064/Work_Stream_2.1_Final.pdf

[SCCI2075]: http://content.digital.nhs.uk/isce/publication/scci2075