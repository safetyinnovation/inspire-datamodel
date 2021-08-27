# Subscription

The event data model will be used to push events like action requests to devices over a WebSocket channel

## Data model

- `subscriptionId`: Unique identifier

- `data`: Array of [Device or Building](https://github.com/inspire-datamodel/SmartBuilding/) containing the newly requested action on the device.