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
 
### FHIR Documents in this Message Specification ###

During interactions between a Hospital and a Local Authority Social Services' team in connection with transfers of care of patients, it may be necessary for either party to send a document embedded within the message. Examples could be letters, assessments or any other relevant supporting information. This specification has included example implementations of the FHIR DocumentReference document format to enable such documents to be sent as outlined below. Where FHIR documents are included, they are contained in separate FHIR bundles within the appropriate Notice or Response bundle.

### Implementation of a FHIR Document Reference ###

This specification allows the inclusion of documents which are non-FHIR based within the message bundle. A pertinent example could be a pdf document requesting further information about a patient or containing other types of supporting information. 
Should this functionality be required, NHS Digital's [Document Reference] specification should be consulted. [ITK-DocumentReference-1] within that specification shows the constraint of the [FHIR DocumentReference resource]. [ITK-DocumentReference-1] details the document and binary attachment structure and provides a common approach for these documents for NHS Digital message flows.
Examples of such implementations showing attached pdfs for a Discharge Notice and a Discharge Notice Accept Response are given in the [Discharge Notice bundle xml example] and the [Discharge Notice Accept Response bundle xml example]. 

For more information on FHIR documents and their implementation, please consult the relevant [FHIR document guidelines].

[Document Header]: https://nhsconnect.github.io/NHS-FHIR-CDA/Generated/Chapter.1.About/index.html
[Document Reference]: https://nhsconnect.github.io/ITK-DocumentReference/Generated/Chapter.1.About/index.html
[ITK-DocumentReference-1]: https://nhsconnect.github.io/ITK-DocumentReference/Generated/Profile.DocumentReference/itk-documentreference-1.html
[COFE-Composition-1]: https://nhsconnect.github.io/NHS-FHIR-CDA/Generated/Profile.DocumentHeader/cofe-composition-1.html
[Assessment Notice bundle xml example]: ../Examples/Profile.ADW-AssessmentNotice/ADW-Message-Assessment-Notice-Bundle-1-Example-1.xml
[FHIR document guidelines]: https://www.hl7.org/fhir/DSTU2/documents.html
[FHIR Composition resource]: http://hl7.org/fhir/DSTU2/composition.html
[FHIR DocumentReference resource]: http://hl7.org/fhir/DSTU2/documentreference.html
[Discharge Notice Accept Response bundle xml example]: ../Examples/Profile.ADW-DischargeNoticeAcceptResponse/ADW-Message-Discharge-Notice-Accept-Response-Bundle-1-Example-1.xml
[Discharge Notice bundle xml example]: ../Examples/Profile.ADW-DischargeNotice/ADW-Message-Discharge-Notice-Bundle-1-Example-1.xml

**Further Information - Contained Element**

Please note that the contained element in the profiles in this specification should not be implemented. 

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

[ADW-AssessmentNotice-MessageHeader-1]: ../Profile.ADW-AssessmentNotice/adw-assessmentnotice-messageheader-1.html




[Profiling FHIR]: http://hl7.org/fhir/DSTU2/profiling.html
[FHIR website]: http://hl7.org/fhir/DSTU2/index.html
[Base Resource Definitions]: http://hl7.org/fhir/DSTU2/resource.html

