# EmergencyVehicle

## Data Model

- `id`

- `type`: EmergencyVehicle

- `name`

- `description`

- `vehicleType`: lorry

- `category`: ["public", "specialUsage"]

- `fleetVehicleId`: Radio call sign of the vehicle

- `vehicleSpecialUsage`: See Vehicle spec.

- `baseStation`: EmergencyStation where this vehicle is usually stationed

- `location`: see Vehicle spec.

- `reportToLocation`: Location to where the vehicle is headed (Optional)

- `assignedToMission`: The link to the mission the EmergencyVehicle is currently assigned to (Optional)

- `deploymentStatus`: See <https://de.wikipedia.org/wiki/Funkmeldesystem#Meldeweg_Fahrzeug_–_Leitstelle>, depends also on `vehicleSpecialUsage`. TODO: Internationalize this, e.g. with DeploymentStatusDefaultValues from EDXL-SitRep
