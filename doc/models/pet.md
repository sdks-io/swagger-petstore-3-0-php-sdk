
# Pet

## Structure

`Pet`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | - | getName(): string | setName(string name): void |
| `photoUrls` | `string[]` | Required | - | getPhotoUrls(): array | setPhotoUrls(array photoUrls): void |
| `id` | `?int` | Optional | - | getId(): ?int | setId(?int id): void |
| `category` | [`?Category`](../../doc/models/category.md) | Optional | - | getCategory(): ?Category | setCategory(?Category category): void |
| `tags` | [`?(Tag[])`](../../doc/models/tag.md) | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `petStatus` | [`?string (PetStatusEnum)`](../../doc/models/pet-status-enum.md) | Optional | pet status in the store | getPetStatus(): ?string | setPetStatus(?string petStatus): void |

## Example (as JSON)

```json
{
  "name": "doggie",
  "photoUrls": [
    "photoUrls5",
    "photoUrls6",
    "photoUrls7"
  ],
  "id": 10,
  "category": {
    "id": 232,
    "name": "name2"
  },
  "tags": [
    {
      "id": 239,
      "name": "name5"
    },
    {
      "id": 240,
      "name": "name6"
    }
  ],
  "petStatus": "pending"
}
```

