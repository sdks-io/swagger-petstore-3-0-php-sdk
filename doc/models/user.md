
# User

## Structure

`User`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?int` | Optional | - | getId(): ?int | setId(?int id): void |
| `username` | `?string` | Optional | - | getUsername(): ?string | setUsername(?string username): void |
| `firstName` | `?string` | Optional | - | getFirstName(): ?string | setFirstName(?string firstName): void |
| `lastName` | `?string` | Optional | - | getLastName(): ?string | setLastName(?string lastName): void |
| `email` | `?string` | Optional | - | getEmail(): ?string | setEmail(?string email): void |
| `password` | `?string` | Optional | - | getPassword(): ?string | setPassword(?string password): void |
| `phone` | `?string` | Optional | - | getPhone(): ?string | setPhone(?string phone): void |
| `userStatus` | `?int` | Optional | User Status | getUserStatus(): ?int | setUserStatus(?int userStatus): void |

## Example (as JSON)

```json
{
  "id": 10,
  "username": "theUser",
  "firstName": "John",
  "lastName": "James",
  "email": "john@email.com",
  "password": "12345",
  "phone": "12345",
  "userStatus": 1
}
```

