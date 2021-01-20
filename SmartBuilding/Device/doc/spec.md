# Device

The data model is adapted from [Smart data model Device](https://github.com/smart-data-models/dataModel.Device) and has some additional properties.

## Data model

- `id`: Unique identifier

- `type`: Device

- `attachedTo`: Relationship. ID of the Building to which this Device is attached to

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
