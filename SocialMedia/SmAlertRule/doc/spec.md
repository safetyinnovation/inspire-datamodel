# SmAlertRule

This entity contains a harmonised description of the datamodel for SmAlertRule. It allows to define simple and complex rules for social media alerts.

## Data Model

- `id`

- `type`: SmAlertRule

- `active`: Boolean. If the alert rule is active.

- `alertConditionOperator`: Enum. Operators for defining alert conditions.  One of `CHANGED`, `EQUAL_TO`, `GREATER_THAN`, `SMALLER_THAN`

- `alertConditionType`: Enum. Type of the alert condition. One of `NUMBER_MENTIONS`, `AVERAGE_SENTIMENT`, `CHANGE_SENTIMENT`, `CHANGE_VOLUME_PERCENTAGE`

- `alertConditionValue`: Number. Value of the alert condition.

- `alertRuleId`: Numner. Addtional id id of an alert rule, e.g. for an external system

- `comparisionTimespanUnit`: Enum. Unit of the comparison timespan. `MONTH`, `WEEK`, `DAY`, `HOUR`, `MINUTE`

- `comparisionTimespanValue`: Number. Value of the comparison timespan.

- `dateLastModified`: Timestamp.

- `deleted`: Boolean. To indicate that the alert rule will be deleted

- `errorMessage`: Text. For potential error messages

- `intervalTimespanUnit`: Enum. Unit of the interval timespan. `MONTH`, `WEEK`, `DAY`, `HOUR`, `MINUTE`

- `intervalTimespanValue`:  Number. Value of the interval timespan.

- `name`: Text. name of the alert rule

- `notificationIntervalUnit`: Enum. Unit of the notification timespan. `MONTH`, `WEEK`, `DAY`, `HOUR`, `MINUTE`

- `notificationIntervalValue`: Number. Value of the notification timespan.

- `searchIds`: Array of Number. List of search ids for which the alert rule is defined
