# Alert

This data model is based on the [Smart Data Model Alert](https://github.com/smart-data-models/dataModel.Alert) and used to describe missions.

## Data model

This variant contains all fields from the parent data model and declares some new ones.

- `data`: StructuredValue
  - `socialMediaSearchIds`: String Array. Indicating which Social Media searches are associated with this Alert
  - `alertKeyWord`: Text. The alert keyword issued for this mission
  - `alertKeyWordShort`: Text. Abbreviation of the alertKeyWord e.g. Fe1C
  - `metaCategory`: Enum. Meta category for this type of mission. Valid values are `FIREFIGHTING`, `CBRN_PROTECTION`, `MEDICAL_EMERGENCY`, `TECHNICAL_SUPPORT`

- `externalId`: Text. Externally assigned ID or mission number for this mission

- `emergencyVehicles`: String Array. List of EmergencyVehicle-IDs associated with this mission.
