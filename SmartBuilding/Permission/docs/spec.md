# Permission



## Data model

- `id`: Unique identifier

- `type`: Device

- `attachedTo`: Relationship. ID of the Building to which this Device is attached to

- `permission`: String. One of `NONE`, `REQUEST`, `PENDING`, `GRANTED` and `DENIED`. `NONE` is the initial state without any permission. `REQUEST` will initiate a permission request from the hub to the smarthome user, which will either be granted immediately or after the smarthome user approves the request. This depends on the chosen security settings. `DENIED` will be returned if the smarthome user denies the request. `PENDING` will be returned if approval is required. `GRANTED` will grant all permissions.