# Motion pattern alert

Data model for a crowd flow motion pattern alert in an ROI.
Currently still under development

## Data model

- `id`: Unique identifier of the entity
- `type`: NGSI Entity type. It has to be CrowdFlowMotionPatternAlert
- `dateObserved`: The date and time of this observation in ISO8601 UTC format.
- `area`: Area inside the ROI in which the density was detected. GeoJSON Polygon.
- `peopleCount`: Number of people forming this pattern
- `motionPatternChangeFrom`: TBD. Previous pattern
- `motionPatternChangeTo`: TBD. Current pattern
- `crowdFlowRoiId`: Associated ROI for this alert
