# Device

The data model is adapted from [Smart data model Device](https://github.com/smart-data-models/dataModel.Device) and has some additional properties.

## Data model

- `id`: Unique identifier

- `type`: Device

- `attachedTo`: Relationship. ID of the Building to which this Device is attached to

- `category`: sensor or actuator 

- `controlledProperty`: For Actuator: door, window, shutter, light

- `configuration`: StructuredValue
  - `profile`: Text. Name of the configuration profile

  - `reportingInterval`: Number. Interval in which device sends new data, in seconds

  - `thresholds`: StructuredValue. Optional. Used for calculating `deviceState`

    - `invalid`: Threshold Configuration Array for invalid state.

      - `comparision`: Text. Comparison Operator. One of `greaterThan`, `greaterThanInclusive`, `lessThan`, `lessThanInclusive`, `equal`, `notEqual`

      - `value`: Number. Threshold level for Invalid state

    - `warning`: Threshold Configuration Array for Warning state. Empty if no Threshold configuration.

      - `comparision`: Text. Comparison Operator. One of `greaterThan`, `greaterThanInclusive`, `lessThan`, `lessThanInclusive`, `equal`, `notEqual`

      - `value`: Number. Threshold level for Warning state

    - `alarm`: Threshold Configuration Array for Alarm state.

      - `comparision`: Text. Comparison Operator. One of `greaterThan`, `greaterThanInclusive`, `lessThan`, `lessThanInclusive`, `equal`, `notEqual`

      - `value`: Number. Threshold level for Alarm state

- `deviceState`: Enum. One of `OK`, `WARNING`, `ALARM`, `ERROR`
- `action`: Only if category is actuator
  - `status`: `PENDING`, `SUCCESS`, `ERROR`, `TIMEOUT`
  - `desiredValue`: see value


- `value`: current status, number, Text (depends on the controlledProperty)
  - `door`: OPEN, CLOSE
  - `window`: OPEN, CLOSE
  - `shutter`: 0-100 (0=open/up, 100=closed/down)
  - `light`: 0-100 (0=off, 100=on)
