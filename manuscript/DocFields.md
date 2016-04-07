#How to Set up Documents to Auto-Populate Fields
You can create fields to auto-populate documents with appropriate data (ex. System, Subsystem, Tag, etc.).  
Fields are indicated with double curly braces, for example, **{{fieldname}}**, without spaces. Recognized fields will be replaced with the appropriate data.

![Sample fields in a check sheet](images\fieldexamples.png)  
*Fields in a check sheet template*

##Common Fields
These fields can be used in any document.

- {{date}} or {{Date}} - date on which the document was generated, in UTC
- {{companyName}} - name of the company on this project
- {{projectName}} - name of the project
- {{projectId}} - internal Id of the project. Should not generally be used except for internal testing purposes

##Check Sheet Fields
These are unique to check sheets or ITRs.

- {{qrcode}} or {{barcode}} - QR code for the document
- {{tagNumber}} - number of the tag, for example, PT-0098
- {{tagDescription}} - description of the tag
- {{tagDiscipline}} - discipline of the tag
- {{tagId}} - internal Id for the tag. Should not generally be used except for internal testing purposes
- {{tagLoopNumber}} - loop, if present, of the tag
- {{tagDrawingNumber}} - drawing number, if present, of the tag
- {{subSystemNumber}} - number of the sub system
- {{subSystemName}} - name of the sub system
- {{systemNumber}} - number of the system
- {{systemName}} - name of the system

##Deficiency Fields
If a deficiency is associated with a tag, all tag fields may also be used.  
If a deficiency is associated with a subsystem or system, fields from both of those may also be used. A deficiency in a subsystem (ex. 120V Power) implies that the same deficiency also applies to the system (ex. Electricity).

- {{deficiencyId}} - internal Id of the deficiency. Should not generally be used excpet for internal testing purposes
- {{deficiencyNumber}} - number of the deficiency
- {{deficiencyType}} - type of the deficiency
- {{deficiencyDescription}} - description of the deficiency
- {{deficiencyCreationDate}} - date the deficiency was created, in UTC
- {{deficiencyExpectedResolutionDate}} - date the deficiency is expected to be complete
- {{deficiencyTitle}} - title of the deficiency
- {{deficiencyWalkdownDate}} - date of the walkdown

##Certificate Fields

- {{certificateName}} - name of the certificate
- {{certificateDiscipline}} - discipline name for the certificate

##Preservation Tokens

- {{preservationRequiredDate}} - required date
- {{preservationNumber}} - number of the preservation
- {{preservationDescription}} - description field from the preservation
- {{preservationStorageRequirements}} - storage requirements; Tag fields may also be used. If the preservation tag is scoped, subsystem and system information is also automatically included
