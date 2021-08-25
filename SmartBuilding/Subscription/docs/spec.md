# Subscription

The event data model will be used to push events like action requests to devices over a WebSocket channel

## Data model

- `subscriptionId`: Unique identifier

- `data`: Array of [Device](https://github.com/inspire-datamodel/SmartBuilding/Devce/docs/spec.md) containing the newly requested action on the device.