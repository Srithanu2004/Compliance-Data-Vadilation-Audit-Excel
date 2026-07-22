# Compliance-Data-Validation-Audit-Excel

![Compliance Data Validation Audit Demo](VIDEO)

*Compliance Data Validation Audit built in Microsoft Excel*

## Project Overview

This project demonstrates how Excel can be used to validate housing compliance data and identify issues before the data is used for reporting.

I used the same synthetic dataset as in my Power BI Compliance & Safety Dashboard, containing 210 properties and 1,758 compliance records.

The goal was to check whether the underlying data was complete, consistent and reliable enough for compliance reporting.

I kept the original data unchanged on separate raw data worksheets and created additional sheets for duplicate checks, missing values, relationship checks, EPC rating validation and audit findings.



## Key Skills Demonstrated

* **Record Count and Duplicate Checks:** I confirmed that all records were transferred into Excel and checked that PropertyID and ComplianceRecordID values were unique in the tables where they were used as key fields.

![Duplicate Key and Record Count Checks](https://github.com/user-attachments/assets/7c9a80c8-63e1-475e-85b5-95ed384a0eb3))

*Duplicate key and record count checks in Excel*


* **XLOOKUP Relationship Check:** I used XLOOKUP to confirm that every PropertyID in the compliance table matched an existing property in the properties table.

![XLOOKUP Property Relationship Check](https://github.com/user-attachments/assets/fc467068-3883-4424-9f6e-8f198fea43c7))

*Validating property relationships using XLOOKUP*


* **Blank and Business Rule Checks:** I used COUNTIFS, IF statements and conditional formatting to identify missing expiry dates and records where a document was marked as received but the ExpiryDate was blank.

![Compliance Validation Checks](https://github.com/user-attachments/assets/d3911566-8d84-4e4a-803d-4b7b140c64ac))

*Audit of blank fields, missing expiry dates and inconsistent statuses*


* **Pivot Table Analysis:** I used a Pivot Table to compare total compliance records with completed expiry dates and identify missing dates by certificate type.

![Pivot Table Analysis](https://github.com/user-attachments/assets/9ca20e12-4b77-4496-abc7-c60bb8676aa9))

*Missing expiry dates by certificate type*


* **EPC Rating Validation:** I checked all EPC records against the expected A–G rating range and confirmed that there were no missing or invalid ratings.

![EPC Rating Validation](https://github.com/user-attachments/assets/6b64c033-d182-42c9-9674-52d68d1ad25b))

*EPC rating validation against the expected A–G range*



## Tools Used

Microsoft Excel, Excel Tables, XLOOKUP, COUNTIF, COUNTIFS, IF statements, Pivot Tables, filtering and conditional formatting.



## Outcome

The final audit result was **Requires Remediation**.

It identified:

* 1,758 compliance records reviewed across 210 properties
* 50 compliance records with a missing ExpiryDate
* 49 records where DocumentReceived was Yes but ExpiryDate was blank
* 37 records where the compliance status did not identify the missing expiry date
* No duplicate PropertyID or ComplianceRecordID key values
* No PropertyIDs in the compliance table that were missing from the properties table
* 218 EPC records with ratings within the valid A–G range

![Compliance Data Validation Audit Summary](https://github.com/user-attachments/assets/0e51ce57-fe28-4489-b74e-5da80f56e732))

*Compliance Data Validation Audit Summary*

The audit showed that some records appeared complete or valid even though important expiry date information was missing.

This project demonstrates practical Excel data validation, housing compliance checks, relationship testing and audit reporting.

