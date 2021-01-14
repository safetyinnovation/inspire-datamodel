# NotificationMessage

The data model is adapted from https://www.schema.org/Message

## Data Model

- `id`

- `type`: NotificationMessage

- `dateSent`: The Timestamp when the message was sent

- `headline`: Text. Short headline text

- `text`: Text. The message content

- `sender`: StructuredValue
  - `id`: ID of the sender
  - `type`: The Type of the sender

- `missionId`: Relationship. The mission with which this message is associated
