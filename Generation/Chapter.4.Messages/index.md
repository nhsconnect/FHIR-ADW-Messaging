# FHIR Messaging #

The FHIR resource profiles within this DMS have been created to support the Assessment, Discharge and Withdrawal Dataset interface for:

 - **[Assessment Notice]** - FHIR resource profiles combined to support the Assessment Notice interface.
 - **[Assessment Notice Accept Response]** - FHIR resource profiles combined to support the Assessment Notice Accept Response interface.
 - **[Assessment Notice Reject Response]** - FHIR resource profiles combined to support the Assessment Notice Reject Response interface.
 - **[Discharge Notice]** - FHIR resource profiles combined to support the Discharge Notice interface.
 - **[Discharge Notice Accept Response]** - FHIR resource profiles combined to support the Discharge Notice Accept Response interface.
 - **[Discharge Notice Reject Response]** - FHIR resource profiles combined to support the Discharge Notice Reject Response interface.
 - **[Withdrawal Notice]** - FHIR resource profiles combined to support the Withdrawal Notice interface.
 - **[Withdrawal Notice Accept Response]** - FHIR resource profiles combined to support the Withdrawal Notice Accept Response interface.
 - **[Withdrawal Notice Reject Response]** - FHIR resource profiles combined to support the Withdrawal Notice Reject Response interface.

## Document Reference ##

This specification allows the inclusion of documents which are non-FHIR based (for example .pdf) within the message bundle. Should this functionality be required, the [COFE-DocumentReference-1] specification should be consulted for guidance on how to create an embedded document in a standard format. The COFE-DocumentReference specification details the document header and binary attachment structure and provides a common approach for embedded documents for NHS Digital message flows.

[COFE-DocumentReference-1]: https://nhsconnect.github.io/NHS-FHIR-CDA-DOCREF/Generated/Chapter.1.About/index.html


**Further Information**

For more information about message profiles visit [Profiling FHIR] and for resource Metadata visit [Base Resource Definitions].

The various downloads (including Schema files) and reference implementations are available on the [FHIR website]. 


[background]: background.html
[Assessment Notice]: ../Profile.ADW-AssessmentNotice/Profile.ADW-AssessmentNotice.html
[Assessment Notice Accept Response]: ../Profile.ADW-AssessmentNoticeAcceptResponse/Profile.ADW-AssessmentNoticeAcceptResponse.html
[Assessment Notice Reject Response]: ../Profile.ADW-AssessmentNoticeRejectResponse/Profile.ADW-AssessmentNoticeRejectResponse.html

[Discharge Notice]: ../Profile.ADW-DischargeNotice/Profile.ADW-DischargeNotice.html
[Discharge Notice Accept Response]: ../Profile.ADW-DischargeNoticeAcceptResponse/Profile.ADW-DischargeNoticeAcceptResponse.html
[Discharge Notice Reject Response]: ../Profile.ADW-DischargeNoticeRejectResponse/Profile.ADW-DischargeNoticeRejectResponse.html

[Withdrawal Notice]: ../Profile.ADW-WithdrawalNotice/Profile.ADW-WithdrawalNotice.html
[Withdrawal Notice Accept Response]: ../Profile.ADW-WithdrawalNoticeAcceptResponse/Profile.ADW-WithdrawalNoticeAcceptResponse.html
[Withdrawal Notice Reject Response]: ../Profile.ADW-WithdrawalNoticeRejectResponse/Profile.ADW-WithdrawalNoticeRejectResponse.html

[ADW-AssessmentNotice-Message-Header-1]: ../Profile.ADW-AssessmentNotice/adw-assessment-notice-message-header-1.html




[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html

