# Participation (Course Enrollments/ECFE Enrollments/Child Care Contracts)

## Get All Participation records

```shell
curl "https://demo.ce.eleyo.com/api/v1/participation/99ea1020-b0d7-0132-3dcd-60030895e8c0"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> The above command returns JSON structured like this:

```json
{
  "participation":[
    "record1",
    "record2...record10"
  ],
  "_metadata":{
    "execution_time":0.024925,
    "time":"2015-03-20T02:48:01Z"
  }
}
```

This endpoint retrieves all participation data for a specific user.

### HTTP Request

`GET https://<DISTRICT>.ce.eleyo.com/api/v1/participation/<USER_ID>`

### URL Parameters

Parameter | Description
--------- | -----------
DISTRICT | The subdomain for your district
USER_ID | The UUID of the user to retrieve data for
