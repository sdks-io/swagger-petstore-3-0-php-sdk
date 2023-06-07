
# Order

## Structure

`Order`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?int` | Optional | - | getId(): ?int | setId(?int id): void |
| `petId` | `?int` | Optional | - | getPetId(): ?int | setPetId(?int petId): void |
| `quantity` | `?int` | Optional | - | getQuantity(): ?int | setQuantity(?int quantity): void |
| `shipDate` | `?DateTime` | Optional | - | getShipDate(): ?\DateTime | setShipDate(?\DateTime shipDate): void |
| `orderStatus` | [`?string (OrderStatusEnum)`](../../doc/models/order-status-enum.md) | Optional | Order Status<br>**Default**: `OrderStatusEnum::APPROVED` | getOrderStatus(): ?string | setOrderStatus(?string orderStatus): void |
| `complete` | `?bool` | Optional | - | getComplete(): ?bool | setComplete(?bool complete): void |

## Example (as JSON)

```json
{
  "id": 10,
  "petId": 198772,
  "quantity": 7,
  "shipDate": "05/31/2023 00:00:00",
  "orderStatus": "approved",
  "complete": true
}
```

