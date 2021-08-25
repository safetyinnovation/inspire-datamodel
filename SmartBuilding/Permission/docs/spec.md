# Permission



## Data model

- `id`: Unique identifier

- `type`: Device

- `attachedTo`: Relationship. ID of the Building to which this Device is attached to

- `permission`: StructuredValue. Explanation of permissions: `LIST` will give access to available devices (name, position, ...) without the current status. `READ` extends the `LIST` permission by the current status. `WRITE` extends the `READ` permission by allowing to set a new value.
  - `*`: Text. Permissions for actuator, sensor and future devices types. One of `LIST`, `READ`, `WRITE`. Allows to define the base permission. Any specific permission specification like `actuator` or `sensor` will take precedence. Defining `WRITE` will still just give `READ` permissions for `sensor`.
  - `actuator`: Text. Permissions for actuator. One of `LIST`, `READ`, `WRITE`. Do not define `actuator` if no specific permission should be given.
  - `sensor`: Text. Permissions for sensor. One of `LIST`, `READ`. Do not define `sensor` if no specific permission should be given.