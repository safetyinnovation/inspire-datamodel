# Velocity alert

Data model for a crowd flow velocity alert in an ROI.
Currently still under development

## Data model

- `id`: Unique identifier of the entity
- `type`: NGSI Entity type. It has to be CrowdFlowVelocityAlert​
- `dateObserved`: The date and time of this observation in ISO8601 UTC format.
- `area`: Area inside the ROI in which the velocity change was detected. GeoJSON Polygon.
- `peopleCount`: Number of people inside the area where a velocity change was detected
- `velocityChange`: Number. Velocity change in m/s, can be positive or negative
- `reasonAlert`: Enum. `velocitySlowerThanMinValue` or `velocityFasterThanMaxValue`
- `crowdFlowRoiId`: Associated ROI for this alert
