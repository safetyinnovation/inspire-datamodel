# UAVCommand

Data model for the command of an UAV

## Data model

- `id`: Unique identifier of the entity
- `type`: NGSI Entity type. It has to be UAVCommand
- `location`: The current location, geojson Point with third parameter as height above ground in meters.
- `command`: Home position of the UAV, geojson Point.
  - `commandName`: Enum. Allowed values `FLY_TO_POI`, `ALARM`
  - `uavPosition`: Point. 3rd parameter, target height in meter above ground. Max height approx 100-120m
- `cameraCommand`: Camera command
  - `cameraCommandName`: Enum. Allowed values: `POI`, `LOOK_TO_GROUND`, `STOW`
  - `cameraImageMode`: Enum. Allowed Values `RGB`, `INFRARED`
  - `cameraPosition`: geojson Point. 3rd parameter camera height, above ground
- `zoomLevel`: Number. 0-100, 0: zoomed out, 100 zoomed in
- `cameraRecording`: Enum. Allowed values: `ON`, if the camera is recording, `OFF` otherwise.
- `doSnapshot`: Boolean. true, to to a snapshot. Attribute needs to be deleted after the snapshot is done
