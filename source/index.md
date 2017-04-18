---
title: API Reference

language_tabs:
  - shell

toc_footers:

includes:
  - participation
  - participation/course_enrollments
  - participation/ecfe_enrollments
  - participation/child_care_contracts
  - errors

search: true
---

# Introduction

Welcome to the Eleyo API Docs.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request

# Client-ID based access
curl "api_endpoint_here"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> Make sure to replace `yourclientid` and `yourclientsecret` with your app's client id and secret.

To access the Eleyo API you must provide your client id and secret via the `Client-ID` and `Client-Secret` HTTP headers.

# Formats

> To specify the data format:

```shell
curl "api_endpoint_here"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -H "Accepts: applicaiton/json"

curl "api_endpoint_here"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
  -H "Accepts: applicaiton/xml"  
```

The api will return `json` or `xml` based on the `Accepts` header. By default the api will return `json`.
