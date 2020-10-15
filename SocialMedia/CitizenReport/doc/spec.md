# CitizenReport

This entity contains a harmonised description of a report send by a citizen via electronic media (i.e. Telegram) and potential further communication between the recipient and the sender.

## Data Model

- `id`

- `type`

- `dateCreated`

- `sender`: URI identifying the sender (e.g. `telegram:xyz`)

- `attachments`
  - Type: `structuredValue`
  - At least one attachment is required
  - Format per attachment
    - `attachmentType`:
      - "TEXT": additional property `text` containing the user-supplied text
      - "IMAGE": additional property `url` containing a URL to the image
      - "VIDEO" additional property `url` containing a URL to the image

- `furtherCommunication`
  - Type: `structuredValue`
  - Format per communication:
    - `direction`: Either `C2A` or `A2C`
    - `dateReceived`: If `direction` is `C2A`, the timestamp when the communication was received
    - `dateSent`: If `direction` is `A2C`, the timestamp when the communication was sent to the citizen
    - `attachment`: One attachment per communication according to the attachment specification

- `location`

  - Attribute type: GeoProperty. `geo:json` Point.
  - Normative References:
        [https://tools.ietf.org/html/rfc7946](https://tools.ietf.org/html/rfc7946)
  - Required.
