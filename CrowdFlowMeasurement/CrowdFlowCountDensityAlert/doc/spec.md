# Count density alert

Data model for a crowd flow density alert in an ROI

## Data model

- `id`: Unique identifier of the entity
- `type`: NGSI Entity type. It has to be CrowdFlowCountDensityAlert
- `dateObserved`: The date and time of this observation in ISO8601 UTC format.
- `area`: Area inside the ROI in which the density was detected. GeoJSON Polygon.
- `peopleDensity`: TBD
- `peopleDensityThreshold`: TBD
- `crowdFlowRoiId`: Associated ROI for this alert
