## All ECFE Enrollments


```shell
curl "https://demo.ce.feepay.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/ecfe_enrollments"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> The above command returns JSON structured like this:

```json

```

This endpoint retrieves a user's ecfe enrollments.

### HTTP Request

`GET https://<DISTRICT>.ce.feepay.com/api/v1/participation/<USER_ID>/ecfe_enrollments`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for

## An ECFE Enrollment


```shell
curl "https://demo.ce.feepay.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/ecfe_enrollments/1"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> The above command returns JSON structured like this:

```json

```

This endpoint retrieves a user's specific ecfe enrollment.

### HTTP Request

`GET https://<DISTRICT>.ce.feepay.com/api/v1/participation/<USER_ID>/ecfe_enrollments/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for
ID | The ID of the ecfe enrollment to retrieve

## An ECFE Enrollment's Question And Answer Responses


```shell
curl "https://demo.ce.feepay.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/ecfe_enrollments/1/responses"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> The above command returns JSON structured like this:

```json

```

This endpoint retrieves a user's specific ecfe enrollment's Question and Answer responses.

### HTTP Request

`GET https://<DISTRICT>.ce.feepay.com/api/v1/participation/<USER_ID>/ecfe_enrollments/<ID>/responses`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for
ID | The ID of the ecfe enrollment to retrieve