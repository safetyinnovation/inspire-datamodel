# Motion change alert

Data model for a crowd flow motion alert in an ROI.
Currently still under development

## Data model

- `id`: Unique identifier of the entity
- `type`: NGSI Entity type. It has to be CrowdFlowMotionChangeAlert
- `dateObserved`: The date and time of this observation in ISO8601 UTC format.
- `area`: Area inside the ROI in which the density was detected. GeoJSON Polygon.
- `motionChangeSeverity`: TBD. Either a number or an enum
- `crowdFlowRoiId`: Associated ROI for this alert
