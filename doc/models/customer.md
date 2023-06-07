
# Customer

## Structure

`Customer`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?int` | Optional | - | getId(): ?int | setId(?int id): void |
| `username` | `?string` | Optional | - | getUsername(): ?string | setUsername(?string username): void |
| `address` | [`?(Address[])`](../../doc/models/address.md) | Optional | - | getAddress(): ?array | setAddress(?array address): void |

## Example (as JSON)

```json
{
  "id": 100000,
  "username": "fehguy",
  "address": [
    {
      "street": "street4",
      "city": "city4",
      "state": "state0",
      "zip": "zip8"
    }
  ]
}
```

