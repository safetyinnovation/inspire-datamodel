# LogBookEntry

The data model represents entries in a (mission) log book. These can be automatic messages, e.g. status changes from vehicles or manual messages.

## Data Model

- `id`: Unique identifier

- `type`: LogBookEntry

- `dateIssued`: The Timestamp when the entry (e.g. the message) was issued

- `messageType`: Enum/String constants to indicate the type of the message e.g. `VEHICLE_STATUS_AT_STATION`, or `MESSAGE` for manual message

- `parameter`: Array. Optional. List of parameter entries for the message
  - `name`: The name of the parameter
  - `value`: The value of the parameter

- `receiver`: Text. Receiver of the message.

- `sender`: StructuredValue
  - `id`: ID of the sender
  - `type`: The Type of the sender
  - `friendlyName`: Descriptive name of the sender

- `text`: Text. Optional. Additional text. Usually only manual messages.

- `missionId`: Relationship. The mission with which this message is associated. Optional.
