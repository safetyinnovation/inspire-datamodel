# CrowdFlowROI

Data Model for a ROI (Region of Interest) for measuring crowd flows in a sub area of a sesor site.

## Data Model

- `id`: Unique identifier
- `type`: CrowdFlowROI
- `sensorSiteId`: Relationship. The id of the associated CrowdflowSensorSite. Designates to which SensorSite this ROI belongs.
- `area`: GeoJson polygon. The Polygon that is the basis of the Region of Interest.
- `edgeIds`: String Array. String Array containing the IDs of the CrowdFlowObserved Objects associated with the edge
- `active`: Boolean. True, if the ROI should be considered for measurements.
- `crowdCountObservedId`: Relationship. The id of the associated CrowdCountObserved
- `displayName`: Text. Name of the ROI
- `edgeNames`: StructuredValue. Mapping between edgeIds and their name.
  - `<id of the edge`: `<edgeName>`
- `crowdFlowVelocityAlertConfig`: Alert configuration for crowdFlowVelocityAlert
  - `peopleRatioThreshold`: Percentage of people in the ROI
  - `active`: Boolean. True, rule activated, false deactived
  - `velocityMinThreshold`: Number in m/s. Lower bound. Alert, if velocity is smaller than this threshold
  - `velocityMaxThreshold`: Number in m/s. Upper bound. Alert, if velocity is greater than this tresholder
- `crowdFlowMotionChangeAlertConfig`: Alert configuration for crowdFlowMotionChangeAlert
  - `sensitivity`: Number. Percentage. TBD.
  - `active`:  Boolean. True, rule activated, false deactived
- `crowdFlowMotionPatternAlertConfig`:  Alert configuration for crowdFlowMotionPatternAlertConfig
  - `active`:  Boolean. True, rule activated, false deactived
  - `pattern`: Array of Enum. Combination of patterns for which an alert should be triggered. Combination of `LAMINAR`, `TURBULENT`, `STELLAR`, `CIRCULAR`
- `crowdCountDensityAlertConfig`: Alert configuration for crowdCountDensityAlertConfig
  - `active`:  Boolean. True, rule activated, false deactived
  - TBD
