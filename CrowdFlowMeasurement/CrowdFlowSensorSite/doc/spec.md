# CrowdFlowSensorSite

Data Model for an area that is covered by crowd flow measurement sensors

## Data Model

- `id`

- `type`: CrowdFlowSensorSite

- `fieldOfView`: GeoJson polygon. Area that is covered by the sensors

- `blindspots`: GeoJson polygon. Blindspots of the sensors in the fieldOfView area

- `sensors`: String Array containing the IDs of the devices. Each device represents a sensor for measuring the crowd flows

