# SocialMediaEvent

This entity contains a harmonised description of a Social Media Event. This data model is related to the `SmAlertRule` datamodel and defines notifications for social media alerts.

## Data Model

- `id`

- `type` : SocialMediaEvent

- `alertRuleName`: Text. Name of the alert rule that triggered

- `dateLastAlerted`: Timestamp. The date and time when the alert rule was satisfied the last time

- `searchIds`: Array of Number. List of search ids for which the event is satisfied

- `searchNames`: Array of Text. List of the search names for which the event is satisified

- `triggeredAlertCondition`: StructuredValue. The details of the alert condition for which this event was raised. See [SMAlertRule](../../SmAlertRule/doc/spec.md) for a description of the properties
  - `alertConditionType`
  - `alertConditionOperator`
  - `alertConditionValue`
  - `intervalTimespanUnit`
  - `comparisionTimespanUnit`
  - `comparisionTimespanValue`
