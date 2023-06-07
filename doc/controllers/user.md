# User

Operations about user

```php
$userController = $client->getUserController();
```

## Class Name

`UserController`

## Methods

* [Create User](../../doc/controllers/user.md#create-user)
* [Create Users With List Input](../../doc/controllers/user.md#create-users-with-list-input)
* [Login User](../../doc/controllers/user.md#login-user)
* [Logout User](../../doc/controllers/user.md#logout-user)
* [Get User by Name](../../doc/controllers/user.md#get-user-by-name)
* [Update User](../../doc/controllers/user.md#update-user)
* [Delete User](../../doc/controllers/user.md#delete-user)


# Create User

This can only be done by the logged in user.

```php
function createUser(
    ?int $id = null,
    ?string $username = null,
    ?string $firstName = null,
    ?string $lastName = null,
    ?string $email = null,
    ?string $password = null,
    ?string $phone = null,
    ?int $userStatus = null
): User
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `?int` | Form, Optional | - |
| `username` | `?string` | Form, Optional | - |
| `firstName` | `?string` | Form, Optional | - |
| `lastName` | `?string` | Form, Optional | - |
| `email` | `?string` | Form, Optional | - |
| `password` | `?string` | Form, Optional | - |
| `phone` | `?string` | Form, Optional | - |
| `userStatus` | `?int` | Form, Optional | User Status |

## Response Type

[`User`](../../doc/models/user.md)

## Example Usage

```php
$id = 10;

$username = 'theUser';

$firstName = 'John';

$lastName = 'James';

$email = 'john@email.com';

$password = '12345';

$phone = '12345';

$userStatus = 1;

$result = $userController->createUser(
    $id,
    $username,
    $firstName,
    $lastName,
    $email,
    $password,
    $phone,
    $userStatus
);
```


# Create Users With List Input

Creates list of users with given input array

```php
function createUsersWithListInput(?array $body = null): User
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?(User[])`](../../doc/models/user.md) | Body, Optional | - |

## Response Type

[`User`](../../doc/models/user.md)

## Example Usage

```php
$result = $userController->createUsersWithListInput();
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | successful operation | `ApiException` |


# Login User

Logs user into the system

```php
function loginUser(?string $username = null, ?string $password = null): string
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `username` | `?string` | Query, Optional | The user name for login |
| `password` | `?string` | Query, Optional | The password for login in clear text |

## Response Type

`string`

## Example Usage

```php
$result = $userController->loginUser();
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username/password supplied | `ApiException` |


# Logout User

Logs out current logged in user session

```php
function logoutUser(): void
```

## Response Type

`void`

## Example Usage

```php
$userController->logoutUser();
```


# Get User by Name

Get user by user name

```php
function getUserByName(string $name): User
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Template, Required | The name that needs to be fetched. Use user1 for testing. |

## Response Type

[`User`](../../doc/models/user.md)

## Example Usage

```php
$name = 'name0';

$result = $userController->getUserByName($name);
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username supplied | `ApiException` |
| 404 | User not found | `ApiException` |


# Update User

This can only be done by the logged in user.

```php
function updateUser(
    string $name,
    ?int $id = null,
    ?string $username = null,
    ?string $firstName = null,
    ?string $lastName = null,
    ?string $email = null,
    ?string $password = null,
    ?string $phone = null,
    ?int $userStatus = null
): void
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Template, Required | name that need to be deleted |
| `id` | `?int` | Form, Optional | - |
| `username` | `?string` | Form, Optional | - |
| `firstName` | `?string` | Form, Optional | - |
| `lastName` | `?string` | Form, Optional | - |
| `email` | `?string` | Form, Optional | - |
| `password` | `?string` | Form, Optional | - |
| `phone` | `?string` | Form, Optional | - |
| `userStatus` | `?int` | Form, Optional | User Status |

## Response Type

`void`

## Example Usage

```php
$name = 'name0';

$id = 10;

$username = 'theUser';

$firstName = 'John';

$lastName = 'James';

$email = 'john@email.com';

$password = '12345';

$phone = '12345';

$userStatus = 1;

$userController->updateUser(
    $name,
    $id,
    $username,
    $firstName,
    $lastName,
    $email,
    $password,
    $phone,
    $userStatus
);
```


# Delete User

This can only be done by the logged in user.

```php
function deleteUser(string $name): void
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Template, Required | The name that needs to be deleted |

## Response Type

`void`

## Example Usage

```php
$name = 'name0';

$userController->deleteUser($name);
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid username supplied | `ApiException` |
| 404 | User not found | `ApiException` |

