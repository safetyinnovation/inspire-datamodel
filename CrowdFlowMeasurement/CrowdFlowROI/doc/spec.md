# CrowdFlowROI

Data Model for a ROI (Region of Interest) for measuring crowd flows in a sub area of a sesor site.

## Data Model

- `id`

- `type`: CrowdFlowROI

- `sensorSiteId`: Relationship. The id of the associated CrowdflowSensorSite. Designates to which SensorSite this ROI belongs.

- `area`: GeoJson polygon. The Polygon that is the basis of the Region of Interest.

- `edgeIds`: String Array. String Array containing the IDs of the CrowdFlowObserved Objects associated with the edge

- `active`: Boolean. True, if the ROI should be considered for measurements.

- `crowdCountObservedId`: Relationship. The id of the associated CrowdCountObserved

- `displayName`: Text. Name of the ROI

- `edgeNames`: StructuredValue. Mapping between edgeIds and their name.
 - `<id of the edge`: `<edgeName>`
 
