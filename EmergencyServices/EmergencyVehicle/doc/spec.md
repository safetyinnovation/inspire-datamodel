# EmergencyVehicle

EmergencyVehicle is based on the FIWARE Vehicle (<https://github.com/smart-data-models/dataModel.Transportation/tree/master/Vehicle>) data model but extends it with emergency-specific information. The extension is based in part on the EDXL-SitRep 1.0 ResouceDetail (4.5.1.1.1) <http://docs.oasis-open.org/emergency/edxl-sitrep/v1.0/cs02/edxl-sitrep-v1.0-cs02.pdf> data type.


## Data Model

- `id`: Unique Identifier

- `type`: EmergencyVehicle

- `name`: Text

- `description`: Text

- `vehicleType`: lorry

- `category`: ["public", "specialUsage"]

- `fleetVehicleId`: Radio call sign of the vehicle

- `vehicleSpecialUsage`: See Vehicle spec.

- `baseStation`: EmergencyStation where this vehicle is usually stationed

- `location`: see Vehicle spec.

- `reportToLocation`: Location to where the vehicle is headed (Optional)

- `assignedToMission`: The link to the mission the EmergencyVehicle is currently assigned to (Optional)

- `deploymentStatus`: See <https://de.wikipedia.org/wiki/Funkmeldesystem#Meldeweg_Fahrzeug_–_Leitstelle>, depends also on `vehicleSpecialUsage`. TODO: Internationalize this, e.g. with DeploymentStatusDefaultValues from EDXL-SitRep
