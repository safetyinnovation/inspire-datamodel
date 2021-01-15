# CrowdCountObserved

Measures the people count in an area

## Data model

- `id`: Unique identifier of the entity
- `type`: NGSI Entity type. It has to be CrowdCountObserved
- `quality`: Accuracy of the detection
- `dateObserved`: The date and time of this observation in ISO8601 UTC format.
- `peopleCount`: Current amount of people in that area
- `totalInbound`: The total number of people who entered the area
- `totalOutbound`: The total number of people who left the area
