# UAVStatus

Data model for the status of an UAV

## Data model

- `id`: Unique identifier of the entity
- `type`: NGSI Entity type. It has to be UAVStatus
- `name`: String. Name of the UAV
- `location`: The current location, geojson Point with third parameter as height above ground in meters.
- `homePosition`: Home position of the UAV, geojson Point.
- `heading`: Number. The heading as degrees clockwise from North
- `groundSpeed`: Number. ground speed of the UAV in m/s
- `vertialSpeed`: Number. vertical speed in m/s (positive = climbing, negative=sinking)
- `flightStatus`: Enum. Allowed values `MISSION`, `HOLD`, `MANUAL`, `RETURN`, `LAND`, `TAKEOFF`
-`isRecordingVideo`: Boolean. truem if the uav's camera is recording a video, false otherwise
- `isArmed`:  Boolean. false, if the uav can be attended safely. true, if the autopilot is ready. The uav cannot be attended safely.
- `fuel`: Number. Battery percentage, 0-100
- `media`: Array of Media elements
  - Format per media element
  - `mediaType`: Enum. Allowed Values `VIDOESTREAM`, `IMAGE`.
  - `url`: Text. The url to the videostream room or to an image
