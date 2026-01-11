Python-based migration tool for converting anonymized RMHC CSV data into FHIR-like JSON format.
The flat legacy CSV (RMHC data) is read row by row and converted into FHIR-compliant JSON resources (Patient and Observation).
Each resource is assigned a unique UUID to ensure distinct identification.
For batch processing, resources are wrapped into a FHIR Transaction Bundle, so all resources are created atomically—either all are successfully saved, or none are, preserving data integrity.
This approach ensures consistent, reproducible migration from legacy CSV to FHIR while maintaining referential integrity between patients and their observations.
