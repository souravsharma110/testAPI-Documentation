# Mappls Pigeon Requirement Documentation

This document covers the requirement for the APIs that are needed in order to complete the product development of the Pigeon.

## Audience Manager
This module will consists of the contacts in the form of Mailing/Recipients lists. Each Mailing/Recipients list will consists of the user data that will further be used to send the email/phone/whatsapp campaigns and workflow automations.

## Recipients List API
The Recipients List API allows you to manage recipient lists for your notifications.

### Get All Recipients Lists
Retrieves a list of all recipient lists in your account. This endpoint returns a list of all recipient lists stored in the system

#### URL:
https://anchor.mappls.com/api/pigeon/audiences/

#### Method:
GET

#### Identity Access Management
A grant type of `Password` is mandatory for this request. What we mean by this is, that a user log-in is mandatory.

> `Authorization` Header needs to be passed with the user `access token` (from Outpost `OAuth 2.0`) to authorize the request.

#### Permissions Required:
anchor.pigeon.audiences.read

#### Success Response
- Code : `200 OK`

    Content: A JSON array of recipient lists, where each recipient list has the following properties:

  - `listId`: A unique identifier for the recipient list (integer).
  - `name`: The name of the recipient list (string).
  - `description`: A brief description of the recipient list (string).
  - `recipientCount`: The number of recipients in the list (integer).

  ```json
  [
      {
          "id": aud00021326456,
          "name": "Mappls Android",
          "description": "List of all Mappls Android users",
          "recipient_count": "250000",
          "created":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          },
          "updated":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          }
      },
      {
          "id": aud00021326456,
          "name": "Mappls iOS",
          "description": "List of all Mappls iOS users",
          "recipient_count": "150002",
          "created":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          },
          "updated":{
            "on": 1600123545,
            "via": "prj00012325564552",
            "by": "usr0012354654123"
          }
      },
      {
        // rest of the mailing lists
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
https://anchor.mappls.com/api/pigeon/audiences/{audienceId}

#### Method:
GET

#### Identity Access Management
A grant type of `Password` is mandatory for this request. What we mean by this is, that a user log-in is mandatory.

> `Authorization` Header needs to be passed with the user `access token` (from Outpost `OAuth 2.0`) to authorize the request.

#### Permissions Required:

`anchor.pigeon.audiences.read`

#### Request Path Parameters:
|   Parameter   |	Type    |	Description |
|   --------    |   ----    |   ----------- |
|   id  |	Integer |	The ID of the recipient list to retrieve. |
|   perPage  |	Integer |	how many results to come in one page. |
|   pageNo  |	Integer |	enter the page no where you directly want to go. |


#### Success Response
- Code : `200 OK`

    Content: A JSON array of recipient lists, where each recipient list has the following properties:

  - `audienceId`: A unique identifier for the recipient list (integer).
  - `name`: The name of the recipient list (string).
  - `description`: A brief description of the recipient list (string).
  - `recipientCount`: The number of recipients in the list (integer).
  - `recipientData`: It will have the reference of user data that has been securely saved in the cache or database.

#### Content Example

  ```json
  {
      "id": "aud00021326456",
      "name": "Mappls Android",
      "recipientCount": "2500000",
      "recipientsData": [
        {
          "Email Address": "sourav@mapmyindia.com",
          "phoneNo": "9818709146",
          "First Name": "Sourav",
          "Last Name": "Sharma",
          "lastEmailSentOn": 1621320002,
          "lastEmailDeliveredOn": 1621320002,
          "lastEmailOpenedOn": 1621320002,
          "createdOn": 16000322312,
          "createdBy": "usr000213155",
          "createdVia": "prj23742838628349"
          //need to check what all information we can have here
        },
        {
          "Email Address": "braj@mapmyindia.com",
          "phoneNo": "9818xxxxxxx",
          "First Name": "Braj",
          "Last Name": "Ankit",
          "lastEmailSentOn": 1621320002,
          "lastEmailDeliveredOn": 1621320002,
          "lastEmailOpenedOn": 1621320002,
          "createdOn": 16000322312,
          "createdBy": "usr000213155",
          "createdVia": "prj23742838628349"
          //need to check what all information we can have here
        }
        //rest data will come here till the pagination
      ],
      "pagination": {
          "totalPages": 4000,
          "itemCount": 10,
          "currentPage": 1,
          "totalItems": 2500000
      }
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
This endpoint allows you to create a new recipient list.

#### URL:
https://anchor.mappls.com/api/pigeon/audiences/

#### Method:
POST

#### Identity Access Management
A grant type of `Password` is mandatory for this request. What we mean by this is, that a user log-in is mandatory.

> `Authorization` Header needs to be passed with the user `access token` (from Outpost `OAuth 2.0`) to authorize the request.

#### Permissions Required:

`anchor.pigeon.audiences.create`

#### Request Body Parameters:
|   Parameter   |	Type    |   Required    |	Description |
|   --------    |   ----    |   ----------- |   ----------- |
|   name  |	String |	Yes |   The name of the recipient list |
|   description  |	String |	No |   The description  of the recipient list |
|   recipientsData  |	array |	No |   The data of the users |

#### Success Response
- Code : `201 Created`

#### Content Example

  ```json
  {
      "name": "Partners",
      "description": "List of all business partners",
      "columnMapping": [
          "Email Address",
          "First Name",
          "Last Name",
          "Phone Number",
          //we can have n number of columns, yes we should have some limits to it
      ],
      "columnValuesAssociated": [
          [
              "sourav@mapmyindia.com",
              "Sourav",
              "Sharma",
              "9818709146"
          ],
          [
              "braj@mapmyindia.com",
              "Braj",
              "Ankit",
              "9818709234"
          ],
          [
              "madhu@mapmyindia.com",
              "Madhu",
              "Singh",
              "9818723444"
          ],
          [
              "deepak.jain@mapmyindia.com",
              "Deepak",
              "Jain",
              "9818349146"
          ]
          //there can be a whole list which can be passed here
      ]
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
https://anchor.mappls.com/api/pigeon/audiences/{audienceId}

#### Method:
PUT

#### Identity Access Management
A grant type of `Password` is mandatory for this request. What we mean by this is, that a user log-in is mandatory.

> `Authorization` Header needs to be passed with the user `access token` (from Outpost `OAuth 2.0`) to authorize the request.

#### Permissions Required:

`anchor.pigeon.audiences.update`

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