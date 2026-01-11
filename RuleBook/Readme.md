FHIR Rulebook containing FHIR Shorthand (FSH) files and SUSHI-generated JSON StructureDefinitions.
“Magic strings” like "M" and "F" can cause inconsistent interpretation of data.
A FHIR ConceptMap was implemented to define explicit mappings from local codes to standard FHIR values ("M" → "male", "F" → "female").
The $translate operation was used at runtime to dynamically convert these codes, ensuring consistent and semantically correct data across all systems.
Cross-Profile References: Observation resources needed to reference Patient profiles, which caused SUSHI compilation errors when custom profiles were not resolved. This was addressed by referencing base FHIR types (Patient) to maintain valid compilation.
