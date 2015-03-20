# Relationships

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