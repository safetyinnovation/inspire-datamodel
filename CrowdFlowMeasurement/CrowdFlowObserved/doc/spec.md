Entity: CrowdFlowObserved
=========================

[Open License](https://github.com/smart-data-models//dataModel.Transportation/blob/master/CrowdFlowObserved/LICENSE.md)

Global description: **CrowdFlowObserved**

## List of properties

- `address`: The mailing address.
- `alternateName`: An alternative name for this item
- `areaServed`: The geographic area where a service or offered item is provided
- `averageCrowdSpeed`: Average speed of the crowd transiting during the observation period
- `averageHeadwayTime`: Average headway time. Headway time is the time
    elapsed between two consecutive persons
- `congested`: Flags whether there was a crowd congestion during the observation period in the referred walkway. The absence of this attribute means no crowd congestion
- `dataProvider`: A sequence of characters identifying the provider of the harmonised data entity.
- `dateCreated`: Entity creation timestamp. This will usually be allocated by the storage platform.
- `dateModified`: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.
- `dateObserved`: The date and time of this observation in ISO8601 UTC format. It can be represented by an specific time instant or by an ISO8601 interval. As a workaround for the lack of support of Orion Context Broker for datetime intervals, it can be used two separate attributes: `dateObservedFrom`, `dateObservedTo`
- `dateObservedFrom`: Observation period start date and time. See `dateObserved`.
- `dateObservedTo`: Observation period end date and time. See `dateObserved`.
- `description`: A description of this item
- `direction`: Usual direction of travel in the walkway referred by this observation with respect to the city center. Enum:'inbound, outbound'
- `id`: Unique identifier of the entity
- `location`:
- `name`: The name of this item.
- `occupancy`: Fraction of the observation time where a person has been occupying the observed walkway
- `owner`: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)
- `peopleCount`: Concerned road segment on which the observation has been made
- `refRoadSegment`: Concerned road segment on which the observation has been made
- `seeAlso`: list of uri pointing to additional resources about the item
- `source`: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.
- `type`: NGSI Entity type. It has to be CrowdFlowObserved

Required properties

- `dateObserved`
- `id`
- `type`

An observation related to the movement of people at a certain place and time.

## Data Model description of properties

Sorted alphabetically (click for details)
<details><summary><strong>full yaml details</strong></summary>

```yaml
CrowdFlowObserved:
  description: CrowdFlowObserved
  properties:
    address:
      description: 'The mailing address.'
      properties:
        addressCountry:
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/Text'''
          type: string
        addressLocality:
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/Text'''
          type: string
        addressRegion:
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/Text'''
          type: string
        areaServed:
          description: 'Property. The geographic area where a service or offered item is provided. Model:''https://schema.org/Text'''
          type: string
        postOfficeBoxNumber:
          description: 'Property. The post office box number for PO box addresses. For example, Spain. Model:''https://schema.org/Text'''
          type: string
        postalCode:
          description: 'Property. The postal code. For example, Spain. Model:''https://schema.org/Text'''
          type: string
        streetAddress:
          description: 'Property. The street address. Model:''https://schema.org/Text'''
          type: string
      type: Property
    alternateName:
      description: 'An alternative name for this item'
      type: Property
    areaServed:
      description: 'The geographic area where a service or offered item is provided'
      type: Property
      x-ngsi:
        model: https://schema.org/Text
    averageCrowdSpeed:
      description: 'Average speed of the crowd transiting during the observation period'
      minimum: 0
      type: Property
      x-ngsi:
        model: https://schema.org/Number
        units: 'Kilometer per hour (Km/h).'
    averageHeadwayTime:
      description: |-
        Average headway time. Headway time is the time
            elapsed between two consecutive persons
      minimum: 0
      type: Property
      x-ngsi:
        model: https://schema.org/Number
        units: 'second (s)'
    congested:
      description: 'Flags whether there was a crowd congestion during the observation period in the referred walkway. The absence of this attribute means no crowd congestion'
      type: Property
      x-ngsi:
        model: https://schema.org/Boolean.
    dataProvider:
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'
      type: Property
    dateCreated:
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'
      format: date-time
      type: Property
    dateModified:
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'
      format: date-time
      type: Property
    dateObserved:
      description: 'The date and time of this observation in ISO8601 UTC format. It can be represented by an specific time instant or by an ISO8601 interval. As a workaround for the lack of support of Orion Context Broker for datetime intervals, it can be used two separate attributes: `dateObservedFrom`, `dateObservedTo`'
      type: Property
      x-ngsi:
        model: https://schema.org/URL.
    dateObservedFrom:
      description: 'Observation period start date and time. See `dateObserved`.'
      format: date-time
      type: Property
      x-ngsi:
        model: https://schema.org/DateTime
    dateObservedTo:
      description: 'Observation period end date and time. See `dateObserved`.'
      format: date-time
      type: Property
      x-ngsi:
        model: https://schema.org/DateTime.
    description:
      description: 'A description of this item'
      type: Property
    direction:
      description: 'Usual direction of travel in the walkway referred by this observation with respect to the city center. Enum:''inbound, outbound'''
      enum:
        - inbound
        - outbound
      type: Property
      x-ngsi:
        model: https://schema.org/Text
    id:
      anyOf: &crowdflowobserved_-_properties_-_owner_-_items_-_anyof
        - description: 'Property. Identifier format of any NGSI entity'
          maxLength: 256
          minLength: 1
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$
          type: string
        - description: 'Property. Identifier format of any NGSI entity'
          format: uri
          type: string
      description: 'Unique identifier of the entity'
      type: Property
    location:
      $id: https://geojson.org/schema/Geometry.json
      $schema: "http://json-schema.org/draft-07/schema#"
      oneOf:
        - properties:
            bbox:
              items:
                type: number
              minItems: 4
              type: array
            coordinates:
              items:
                type: number
              minItems: 2
              type: array
            type:
              enum:
                - Point
              type: string
          required:
            - type
            - coordinates
          title: 'GeoJSON Point'
          type: object
        - properties:
            bbox:
              items:
                type: number
              minItems: 4
              type: array
            coordinates:
              items:
                items:
                  type: number
                minItems: 2
                type: array
              minItems: 2
              type: array
            type:
              enum:
                - LineString
              type: string
          required:
            - type
            - coordinates
          title: 'GeoJSON LineString'
          type: object
        - properties:
            bbox:
              items:
                type: number
              minItems: 4
              type: array
            coordinates:
              items:
                items:
                  items:
                    type: number
                  minItems: 2
                  type: array
                minItems: 4
                type: array
              type: array
            type:
              enum:
                - Polygon
              type: string
          required:
            - type
            - coordinates
          title: 'GeoJSON Polygon'
          type: object
        - properties:
            bbox:
              items:
                type: number
              minItems: 4
              type: array
            coordinates:
              items:
                items:
                  type: number
                minItems: 2
                type: array
              type: array
            type:
              enum:
                - MultiPoint
              type: string
          required:
            - type
            - coordinates
          title: 'GeoJSON MultiPoint'
          type: object
        - properties:
            bbox:
              items:
                type: number
              minItems: 4
              type: array
            coordinates:
              items:
                items:
                  items:
                    type: number
                  minItems: 2
                  type: array
                minItems: 2
                type: array
              type: array
            type:
              enum:
                - MultiLineString
              type: string
          required:
            - type
            - coordinates
          title: 'GeoJSON MultiLineString'
          type: object
        - properties:
            bbox:
              items:
                type: number
              minItems: 4
              type: array
            coordinates:
              items:
                items:
                  items:
                    items:
                      type: number
                    minItems: 2
                    type: array
                  minItems: 4
                  type: array
                type: array
              type: array
            type:
              enum:
                - MultiPolygon
              type: string
          required:
            - type
            - coordinates
          title: 'GeoJSON MultiPolygon'
          type: object
      title: 'GeoJSON Geometry'
    name:
      description: 'The name of this item.'
      type: Property
    occupancy:
      description: 'Fraction of the observation time where a person has been occupying the observed walkway'
      maximum: 1
      minimum: 0
      type: Property
      x-ngsi:
        model: https://schema.org/Number)
    owner:
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'
      items:
        anyOf: *crowdflowobserved_-_properties_-_owner_-_items_-_anyof
        description: 'Property. Unique identifier of the entity'
      type: Property
    peopleCount:
      description: 'Concerned road segment on which the observation has been made'
      minimum: 0
      type: Property
      x-ngsi:
        model: https://schema.org/Number.
    refRoadSegment:
      anyOf:
        - description: 'Property. Identifier format of any NGSI entity'
          maxLength: 256
          minLength: 1
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$
          type: string
        - description: 'Property. Identifier format of any NGSI entity'
          format: uri
          type: string
      description: 'Concerned road segment on which the observation has been made'
      type: Relationship
      x-ngsi:
        model: https://schema.org/URL.
    seeAlso:
      description: 'list of uri pointing to additional resources about the item'
      oneOf:
        - items:
            - format: uri
              type: string
          minItems: 1
          type: array
        - format: uri
          type: string
      type: Property
    source:
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'
      type: Property
    type:
      description: 'NGSI Entity type. It has to be CrowdFlowObserved'
      enum:
        - CrowdFlowObserved
      type: Property
  required:
    - id
    - type
    - dateObserved
  type: object
```

</details>

## Example payloads

#### CrowdFlowObserved NGSI V2 key-values Example

Here is an example of a CrowdFlowObserved in JSON format as key-values. This is compatible with NGSI V2 when  using `options=keyValues` and returns the context data of an individual entity.

```json

{
  "id": "urn:ngsi-ld:CrowdFlowObserved:Valladolid_1",
  "type": "CrowdFlowObserved",
  "dateObserved": "2018-08-07T11:10:00/2018-08-07T11:15:00",
  "dateObservedFrom": "2018-08-07T11:10:00Z",
  "dateObservedTo": "2018-08-07T11:15:00Z",
  "peopleCount": 100,
  "averageHeadwayTime": 5,
  "congested": false,
  "direction": "inbound",
  "location": {
    "type": "LineString",
    "coordinates": [
      [-4.73735395519672, 41.6538181849672],
      [-4.73414858659993, 41.6600594193478],
      [-4.73447575302641, 41.659585195093]
    ]
  }
}
```

#### CrowdFlowObserved NGSI V2 normalized Example

Here is an example of a CrowdFlowObserved in JSON format as normalized. This is compatible with NGSI V2 when not using options and returns the context data of an individual entity.

```json

{
  "id": "urn:ngsi-ld:CrowdFlowObserved:Valladolid_1",
  "type": "CrowdFlowObserved",
  "dateObserved": {
    "value": "2018-08-07T11:10:00/2018-08-07T11:15:00"
  },
  "direction": {
    "value": "inbound"
  },
  "dateObservedFrom": {
    "type": "DateTime",
    "value": "2018-08-07T11:10:00Z"
  },
  "peopleCount": {
    "value": 100
  },
  "averageHeadwayTime": {
    "value": 5
  },
  "dateObservedTo": {
    "type": "DateTime",
    "value": "2018-08-07T11:15:00Z"
  },
  "location": {
    "type": "geo:json",
    "value": {
      "type": "LineString",
      "coordinates": [
        [-4.73735395519672, 41.6538181849672],
        [-4.73414858659993, 41.6600594193478],
        [-4.73447575302641, 41.659585195093]
      ]
    }
  },
  "congested": {
    "value": false
  }
}
```

#### CrowdFlowObserved NGSI-LD key-values Example

Here is an example of a CrowdFlowObserved in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.

```json

{"@context": ["https://schema.lab.fiware.org/ld/context",
              "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"],
 "averageHeadwayTime": 5,
 "congested": False,
 "dateObserved": "2018-08-07T11:10:00/2018-08-07T11:15:00",
 "dateObservedFrom": {"@type": "DateTime", "@value": "2018-08-07T11:10:00Z"},
 "dateObservedTo": {"@type": "DateTime", "@value": "2018-08-07T11:15:00Z"},
 "direction": "inbound",
 "id": "urn:ngsi-ld:CrowdFlowObserved:Valladolid_1",
 "location": {"coordinates": [[-4.73735395519672, 41.6538181849672],
                              [-4.73414858659993, 41.6600594193478],
                              [-4.73447575302641, 41.659585195093]],
              "type": "LineString"},
 "peopleCount": 100,
 "type": "CrowdFlowObserved"}
```

#### CrowdFlowObserved NGSI-LD normalized Example

Here is an example of a CrowdFlowObserved in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.

```json

{
    "id": "urn:ngsi-ld:CrowdFlowObserved:Valladolid_1",
    "type": "CrowdFlowObserved",
    "dateObserved": {
        "type": "Property",
        "value": "2018-08-07T11:10:00/2018-08-07T11:15:00"
    },
    "direction": {
        "type": "Property",
        "value": "inbound"
    },
    "dateObservedFrom": {
        "type": "Property",
        "value": {
            "@type": "DateTime",
            "@value": "2018-08-07T11:10:00Z"
        }
    },
    "peopleCount": {
        "type": "Property",
        "value": 100
    },
    "averageHeadwayTime": {
        "type": "Property",
        "value": 5
    },
    "dateObservedTo": {
        "type": "Property",
        "value": {
            "@type": "DateTime",
            "@value": "2018-08-07T11:15:00Z"
        }
    },
    "location": {
        "type": "GeoProperty",
        "value": {
            "type": "LineString",
            "coordinates": [
                [
                    -4.73735395519672,
                    41.6538181849672
                ],
                [
                    -4.73414858659993,
                    41.6600594193478
                ],
                [
                    -4.73447575302641,
                    41.659585195093
                ]
            ]
        }
    },
    "congested": {
        "type": "Property",
        "value": false
    },
    "@context": [
        "https://schema.lab.fiware.org/ld/context",
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"
    ]
}
```
