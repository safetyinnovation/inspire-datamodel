# NotificationMessage

The data model is adapted from [Schema.org/Message](https://www.schema.org/Message)

## Data Model

- `id`: Uniqzue identifier

- `type`: NotificationMessage

- `dateSent`: The Timestamp when the message was sent

- `headline`: Text. Short headline text

- `text`: Text. The message content

- `sender`: StructuredValue
  - `id`: ID of the sender
  - `type`: The Type of the sender

- `missionId`: Relationship. The mission with which this message is associated. Optional.
