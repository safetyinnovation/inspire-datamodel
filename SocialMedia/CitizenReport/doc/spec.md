# CitizenReport

This entity contains a harmonised description of a report send by a citizen via electronic media (i.e. Telegram) and a potential answer by the authorities.

## Data Model

- `id`

- `type`

- `dateCreated`

- `sender`: 
   - `id`: ID of the sender
   - `name`: Name of the sender

- `attachments`
  - Type: `structuredValue`
  - At least one attachment is required
  - Format per attachment
    - `attachmentType`:
      - "TEXT": additional property `text` containing the user-supplied text
      - "IMAGE": additional property `url` containing a URL to the image
      - "VIDEO": additional property `url` containing a URL to the image
      - "VIDEO" addtional property `extra`, containing addtional information e.g. a thumbnail url

- `answer` (Optional)
  - Type: `structuredValue`
  - `dateSent`: The timestamp when the communication was actually sent to the citizen, non existent if not sent yet
  - `text`: Text sent by the authorities

- `location`

  - Attribute type: GeoProperty. `geo:json` Point.
  - Normative References:
        [https://tools.ietf.org/html/rfc7946](https://tools.ietf.org/html/rfc7946)
  - Required.
