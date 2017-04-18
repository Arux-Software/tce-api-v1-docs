## All Course Enrollments


```shell
curl "https://demo.ce.eleyo.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/course_enrollments"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

This endpoint retrieves a specific user's course enrollments.

### HTTP Request

`GET https://<DISTRICT>.ce.eleyo.com/api/v1/participation/<USER_ID>/course_enrollments`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for

## A Course Enrollment


```shell
curl "https://demo.ce.eleyo.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/course_enrollments/1"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

This endpoint retrieves a user's specific course enrollment.

### HTTP Request

`GET https://<DISTRICT>.ce.eleyo.com/api/v1/participation/<USER_ID>/course_enrollments/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for
ID | The ID of the course enrollment to retrieve

## A Course Enrollment's Question And Answer Responses


```shell
curl "https://demo.ce.eleyo.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0/course_enrollments/1/responses"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

This endpoint retrieves a user's specific course enrollment's Question and Answer responses.

### HTTP Request

`GET https://<DISTRICT>.ce.eleyo.com/api/v1/participation/<USER_ID>/course_enrollments/<ID>/responses`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for
ID | The ID of the course enrollment to retrieve