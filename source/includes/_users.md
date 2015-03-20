# Users (People)

## Get All Users

```shell
curl "https://accounts.feepay.switchboard.io/api/v1/users"
  -H "Authorization: theoauth2accesstoken"
```

> The above command returns JSON structured like this:

```json
{
  "users":[
    "user1",
    "user3...user20"
  ],
  "_metadata":{
    "page":1,
    "per_page":20,
    "total_count":2316,
    "total_pages":116,
    "next_page_uri":"https://accounts...io/api/v1/users?page=2&per_page=20",
    "execution_time":0.024925,
    "time":"2015-03-20T02:48:01Z"
  }
}
```

This endpoint retrieves all users your OAuth or Client-ID have access to.

### HTTP Request

`GET https://accounts.feepay.switchboard.io/api/v1/users`

### Available Search Parameters

`Date`, `Datetime`, and `Year` types are range searchable fields. They can be searched using `.gt` (greater than) and `.lt` (less than) in addition to exact matches.

Parameter | Type | Possible Values
--------- | ------- | -----------
first_name | String | 
middle_name | String |
last_name | String |
nick_name | String |
email_address | String |
phone_number | String |
address | String |
birth_date | Date |
birth_date.lt | Date |
birth_date.gt | Date |
due_date | Date |
due_date.lt | Date |
due_date.gt | Date |
grade_graduation_year | Year |
grade_graduation_year.lt | Year |
grade_graduation_year.gt | Year |
gender | String | `Male`, `Female`
created_at | DateTime |
created_at.lt | DateTime |
created_at.gt | DateTime |
updated_at | DateTime |
updated_at.lt | DateTime |
updated_at.gt | DateTime |

## Get a Specific User


```shell
curl "https://accounts.feepay.switchboard.io/api/v1/users/99ea1020-b0d7-0132-3dcd-60030895e8c0"
  -H "Authorization: theoauth2accesstoken"
```

> The above command returns JSON structured like this:

```json
{
  "user": {
    "uuid": "da3b6350-b0d8-0132-3dcd-60030895e8c0",
    "alternate_uuids": [
      "dc0ebe90-b0d8-0132-3dcd-60030895e8c0"
    ],
    "district_uuids": [
      {
        "uuid": "99ea1020-b0d7-0132-3dcd-60030895e8c0",
        "district": {
          "name": "Test Public School District",
          "sn": "NA-TEST-987"
        }
      }
    ],
    "external_ids": [
      {
        "identifier": "012345",
        "identifier_type": "SIS",
        "context": "NA-TEST-987"
      },
      {
        "identifier": "3518075930432",
        "identifier_type": "STATE",
        "context": "MN"
      }
    ],
    "first_name": "Bill",
    "last_name": "Lumberg",
    "middle_name": null,
    "nick_name": null,
    "gender": null,
    "birth_date": null,
    "due_date": null,
    "grade_graduation_year": null,
    "special_needs": null,
    "hispanic_or_latino": false,
    "race": [],
    "image": null,
    "addresses": [],
    "phone_numbers": [
      {
        "phone_number": "5555555555",
        "extension": null,
        "phone_type": "Home",
        "receive_text_messages": false,
        "primary": true,
        "verified": false,
        "verified_at": null,
        "created_at": "2015-03-20T02:38:08Z",
        "active": true
      }
    ],
    "email_addresses": [
      {
        "email_address": "bill@example.com",
        "primary": true,
        "verified": true,
        "verified_at": "2015-02-04T03:54:36Z",
        "created_at": "2015-02-03T03:55:28Z",
        "active": true
      }
    ],
    "receive_marketing_email": true,
    "active": true,
    "created_at": "2015-02-03T03:55:28Z",
    "updated_at": "2015-03-20T03:55:46Z",
    "deleted_at": null,
    "relationship_details": []
  },
  "_metadata": {
    "execution_time": 0.077969,
    "time": "2015-03-20T04:05:37Z"
  }
}
```

This endpoint retrieves a specific user.

<aside class="notice">If you are using an OAuth token you will only be able to access the spcific user's and any of their relationship's information.</aside>

### HTTP Request

`GET https://accounts.feepay.switchboard.io/api/v1/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The UUID of the user to retrieve

## Create a new User

```shell
curl "https://accounts.feepay.switchboard.io/api/v1/users"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -X POST -d <POST DATA>
```

This endpoint creates a new user.

### HTTP Request

`POST https://accounts.feepay.switchboard.io/api/v1/users`

<aside class="warning">This method is currently not available in v1</aside>

## Update a User

```shell
curl "https://accounts.feepay.switchboard.io/api/v1/users/99ea1020-b0d7-0132-3dcd-60030895e8c0"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -X PUT -d <POST DATA>
```

This endpoint updates a user.

### HTTP Request

`PUT https://accounts.feepay.switchboard.io/api/v1/users/<ID>`

<aside class="warning">This method is currently not available in v1</aside>

### URL Parameters

Parameter | Description
--------- | -----------
ID | The UUID of the user to update

## Delete a User

```shell
curl "https://accounts.feepay.switchboard.io/api/v1/users/99ea1020-b0d7-0132-3dcd-60030895e8c0"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -X DELETE
```

This endpoint deletes a user.

### HTTP Request

`DELETE https://accounts.feepay.switchboard.io/api/v1/users/<ID>`

<aside class="warning">This method is currently not available in v1</aside>

### URL Parameters

Parameter | Description
--------- | -----------
ID | The UUID of the user to delete

## Merge two Users

```shell
curl "https://accounts.feepay.switchboard.io/api/v1/users/merge/99ea1020-b0d7-0132-3dcd-60030895e8c0/fbd482b0-b0dc-0132-3dcd-60030895e8c0"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -X PUT
```

This endpoint deletes a user.

### HTTP Request

`PUT https://accounts.feepay.switchboard.io/api/v1/users/merge/<ID1>/<ID2>`

<aside class="notice">When merging two users the resulting user will recive all UUIDs assigned to both users, including district specific UUIDs. The primary UUID of the merged user will be the first uuid passed to the endpoint</aside>

<aside class="warning">This method is currently not available in v1</aside>

### URL Parameters

Parameter | Description
--------- | -----------
ID1 | The UUID of the user to merge into
ID2 | The UUID of the user to merge data from and remove


## Relationships

Available Relationship types are:

`Spouse`, `Significant Other`,
`Child`, `Foster Child`, `Grandchild`, 
`Parent`, `Foster Parent`, `Grandparent`, 
`Emergency Contact`, `Sibling`, `Friend`, `Other`

## Create or Update a relationship

```shell
curl "https://accounts.feepay.switchboard.io/api/v1/relationships/99ea1020-b0d7-0132-3dcd-60030895e8c0/fbd482b0-b0dc-0132-3dcd-60030895e8c0/friend"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -X PUT
```

This endpoint creates or updates a relationship between two users.
It will automatically create an inverse relationship for new `Child` and `Parent` type relationships.

### HTTP Request

`PUT https://accounts.feepay.switchboard.io/api/v1/relationships/<ID1>/<ID2>/<Type>`

<aside class="warning">This method is currently not available in v1 and is subject to change</aside>

### URL Parameters

Parameter | Description
--------- | -----------
ID1 | The UUID of the first user 
ID2 | The UUID of the second user 
Type | The type of relationship

### Optional Parameters

Parameter | Type | Description
--------- | ----------- | -----------
lives_with | Boolean | The two users live with eachother
emergency_contact | Boolean | <ID1> is an emergency contact of <ID2>

## Delete a relationship

```shell
curl "https://accounts.feepay.switchboard.io/api/v1/relationships/99ea1020-b0d7-0132-3dcd-60030895e8c0/fbd482b0-b0dc-0132-3dcd-60030895e8c0/friend"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -X DELETE
```

This endpoint deletes the relationships between two users.

### HTTP Request

`DELETE https://accounts.feepay.switchboard.io/api/v1/relationships/<ID1>/<ID2>/<Type>`

<aside class="warning">This method is currently not available in v1 and is subject to change</aside>

### URL Parameters

Parameter | Description
--------- | -----------
ID1 | The UUID of the first user 
ID2 | The UUID of the second user 
Type | The type of relationship
