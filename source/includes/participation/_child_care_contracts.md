## All Child Care Contracts


```shell
curl "https://demo.ce.feepay.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/child_care_contracts"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> The above command returns JSON structured like this:

```json

```

This endpoint retrieves a specific user's child care contracts.

### HTTP Request

`GET https://<DISTRICT>.ce.feepay.com/api/v1/participation/<USER_ID>/child_care_contracts`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for

## A Child Care Contract


```shell
curl "https://demo.ce.feepay.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/child_care_contracts/1"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> The above command returns JSON structured like this:

```json

```

This endpoint retrieves a user's specific child care contract.

### HTTP Request

`GET https://<DISTRICT>.ce.feepay.com/api/v1/participation/<USER_ID>/child_care_contracts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for
ID | The ID of the child care contract to retrieve

## A Child Care Contract's Question And Answer Responses


```shell
curl "https://demo.ce.feepay.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/child_care_contracts/1/responses"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> The above command returns JSON structured like this:

```json

```

This endpoint retrieves a user's specific child care contract's Question and Answer responses.

### HTTP Request

`GET https://<DISTRICT>.ce.feepay.com/api/v1/participation/<USER_ID>/child_care_contracts/<ID>/responses`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for
ID | The ID of the child care contract to retrieve