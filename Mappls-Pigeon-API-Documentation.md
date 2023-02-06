# Mappls Pigeon API Documentation

## Recipients List API
The Recipients List API allows you to manage recipient lists for your notifications.

### Get All Recipients Lists
Retrieves a list of all recipient lists in your account. This endpoint returns a list of all recipient lists stored in the system

#### URL:
/recipients_lists

#### Method:
GET

#### Auth Required:
Yes

#### Permissions Required:
View Recipients Lists

#### Success Response
- Code : `200 OK`

    Content: A JSON array of recipient lists, where each recipient list has the following properties:

  - `id`: A unique identifier for the recipient list (integer).
  - `name`: The name of the recipient list (string).
  - `description`: A brief description of the recipient list (string).
  - `recipient_count`: The number of recipients in the list (integer).

```json
[
    {
        "id": 1,
        "name": "Customers",
        "description": "List of all customers",
        "created_at": "2022-12-01T12:00:00Z",
        "updated_at": "2022-12-01T12:00:00Z"
    },
    {
        "id": 2,
        "name": "Subscribers",
        "description": "List of all newsletter subscribers",
        "created_at": "2022-12-02T12:00:00Z",
        "updated_at": "2022-12-02T12:00:00Z"
    }
]
```
- Code: `401 Unauthorized`

    Content:
```json
{
  "error": "Unauthorized access"
}
```
- Code: `403 Forbidden`

    Content:
```json
{
  "error": "Access denied, insufficient permissions"
}
```


### Get Recipient List by ID
Retrieves a recipient list by ID. This endpoint returns a specific recipient list based on its ID.

#### URL:
/recipients_lists/:id

#### Method:
GET

#### Auth Required:
Yes

#### Permissions Required:
View Recipients Lists

#### Request Path Parameters:
|   Parameter   |	Type    |	Description |
|   --------    |   ----    |   ----------- |
|   id  |	Integer |	The ID of the recipient list to retrieve. |

#### Success Response
- Code : `200 OK`

    Content: A JSON array of recipient lists, where each recipient list has the following properties:

  - `id`: A unique identifier for the recipient list (integer).
  - `name`: The name of the recipient list (string).
  - `description`: A brief description of the recipient list (string).
  - `recipient_count`: The number of recipients in the list (integer).

#### Content Example

```json
{
    "id": 1,
    "name": "Customers",
    "description": "List of all customers",
    "created_at": "2022-12-01T12:00:00Z",
    "updated_at": "2022-12-01T12:00:00Z"
}
```

- Code: `401 Unauthorized`

    Content:
```json
{
  "error": "Unauthorized access"
}
```
- Code: `403 Forbidden`

    Content:
```json
{
  "error": "Access denied, insufficient permissions"
}
```

### Create Recipient List
Creates a recipient list by ID. This endpoint allows you to create a new recipient list.

#### URL:
/recipients_lists/

#### Method:
POST

#### Auth Required:
Yes

#### Permissions Required:
Create Recipients Lists

#### Request Body Parameters:
|   Parameter   |	Type    |   Required    |	Description |
|   --------    |   ----    |   ----------- |   ----------- |
|   name  |	String |	Yes |   The name of the recipient list |
|   description  |	String |	No |   The description  of the recipient list |

#### Success Response
- Code : `201 Created`

#### Content Example

```json
{
    "name": "Partners",
    "description": "List of all business partners"
}
```

- Code: `401 Unauthorized`

    Content:
```json
{
  "error": "Unauthorized access"
}
```
- Code: `403 Forbidden`

    Content:
```json
{
  "error": "Access denied, insufficient permissions"
}
```

### Update Recipient List
Updates a recipient list by ID.

#### URL:
/api/recipient_lists/:id/

#### Method:
PUT

#### Auth Required:
Yes

#### Permissions Required:
Update Recipients Lists

#### Request Body Parameters:
|   Parameter   |	Type    |   Required    |	Description |
|   --------    |   ----    |   ----------- |   ----------- |
|   name  |	String |	Yes |   The name of the recipient list |
|   description  |	String |	No |   The description  of the recipient list |

#### Success Response
- Code : `200 OK`

#### Content Example

```json
{
    "name": "Partners",
    "description": "List of all business partners"
}
```

- Code: `401 Unauthorized`

    Content:
```json
{
  "error": "Unauthorized access"
}
```
- Code: `403 Forbidden`

    Content:
```json
{
  "error": "Access denied, insufficient permissions"
}
```

### Delete Recipient List
Deletes a recipient list by ID.

#### URL:
/api/recipient_lists/:id/

#### Method:
DELETE

#### Auth Required:
Yes

#### Permissions Required:
Delete Recipients Lists

#### Request Body Parameters:
|   Parameter   |	Type    |   Required    |	Description |
|   --------    |   ----    |   ----------- |   ----------- |
|   name  |	String |	Yes |   The name of the recipient list |
|   description  |	String |	No |   The description  of the recipient list |

#### Success Response
- Code : `204 No Content`

- Code: `401 Unauthorized`

    Content:
```json
{
  "error": "Unauthorized access"
}
```
- Code: `403 Forbidden`

    Content:
```json
{
  "error": "Access denied, insufficient permissions"
}
```