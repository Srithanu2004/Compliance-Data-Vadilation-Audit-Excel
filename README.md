#  Compliance Data Validation Audit Excel

![Compliance Data Validation Audit Demo](https://github.com/user-attachments/assets/4ec1e825-7da1-4497-bff6-4d68d63d0c21)

*Compliance Data Validation Audit built in Microsoft Excel*


## Project Overview

This project demonstrates how Excel can be used to validate housing compliance data and identify issues before the data is used for reporting.

I used the same synthetic dataset as in my [Power BI Compliance & Safety Dashboard](https://github.com/EkatarinaMail/Housing-Compliance-Dashboard-PowerBI-SQL), containing 210 properties and 1,758 compliance records.

The goal was to check whether the underlying data was complete, consistent and reliable enough for compliance reporting.

I kept the original data unchanged on separate raw data worksheets and created additional sheets for duplicate checks, missing values, relationship checks, EPC rating validation and audit findings.


## Key Skills Demonstrated

* **Record Count and Duplicate Checks:** I confirmed that all records were transferred into Excel and checked that PropertyID and ComplianceRecordID values were unique in the tables where they were used as key fields.

![Duplicate Key and Record Count Checks](https://github.com/user-attachments/assets/6555948f-cced-4699-8435-f9ac7100fe80)
*Duplicate key and record count checks in Excel*

* **XLOOKUP Relationship Check:** I used XLOOKUP to confirm that every PropertyID in the compliance table matched an existing property in the properties table.

![XLOOKUP Property Relationship Check](https://github.com/user-attachments/assets/25a65fff-34bc-4235-996b-9b68987469a9)
*Validating property relationships using XLOOKUP*

* **Blank and Business Rule Checks:** I used COUNTIFS, IF statements and conditional formatting to identify missing expiry dates and records where a document was marked as received but the ExpiryDate was blank.

![Blank and Business Rule Checks](https://github.com/user-attachments/assets/d438a93a-67bd-45dd-95dd-bed1210d873f)
*Audit of blank fields, missing expiry dates and inconsistent statuses*

* **Pivot Table Analysis:** I used a Pivot Table to compare total compliance records with completed expiry dates and identify missing dates by certificate type.

![Pivot Table Analysis](https://github.com/user-attachments/assets/f58ed3ed-58e9-4149-b7f7-5f8d01ec90aa)
*Missing expiry dates by certificate type*

* **EPC Rating Validation:** I checked all EPC records against the expected A–G rating range and confirmed that there were no missing or invalid ratings.

![EPC Rating Validation](https://github.com/user-attachments/assets/a272d976-8dd7-48c2-9e2e-1269b1ecfec7)
*EPC rating validation against the expected A–G range*


## Tools Used

Microsoft Excel, Excel Tables, XLOOKUP, COUNTIF, COUNTIFS, IF statements, Pivot Tables, filtering and conditional formatting.


## Outcome

The audit identified several data quality issues that required remediation before the data could be relied upon for reporting.

It identified:

* 1,758 compliance records reviewed across 210 properties
* 50 records with a missing ExpiryDate
* 49 of these records were marked as DocumentReceived = Yes and 1 as No
* 13 missing expiry dates were correctly flagged, while 37 were not identified by status
* No duplicate PropertyID or ComplianceRecordID values
* No PropertyIDs missing from the properties table
* 218 EPC records with valid A–G ratings


![Compliance Data Validation Audit Summary](https://github.com/user-attachments/assets/ca703b10-d63e-4868-9a9f-56b96a30a8e8)
*Compliance Data Validation Audit Summary*

The audit showed that some records appeared complete even though important expiry date information was missing.

This project demonstrates practical Excel data validation, housing compliance checks, relationship testing and audit reporting.


## Related Projects

[View the Compliance & Safety Dashboard - Power BI & SQL](https://github.com/EkatarinaMail/Housing-Compliance-Dashboard-PowerBI-SQL)

[View the Housing Data Reconciliation & Exception Audit - Excel](https://github.com/EkatarinaMail/Housing-Data-Reconciliation-Exception-Audit-Excel)


