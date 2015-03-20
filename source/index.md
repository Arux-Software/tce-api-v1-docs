---
title: API Reference

language_tabs:
  - shell

toc_footers:

includes:
  - oauth
  - users
  - cart
  - errors

search: true
---

# Introduction

Welcome to the FeePay Switchboard API Docs.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
# OAuth2 based access
curl "api_endpoint_here"
  -H "Authorization: theoauth2accesstoken"
  
# Client-ID based access
curl "api_endpoint_here"
  -H "Client-ID: yourclientid" -H "Client-Secret: yourclientsecret"
```

> Make sure to replace `theoauth2accesstoken` with the user's Oauth2 Access Token or `yourclientid` and `yourclientsecret` with your app's client id and secret.

There are two ways to authenticate and get data from the API. 

1. Using an oauth2 access token granted to your app when a user logs in via oauth2. Provide the access token via the `Authorization` HTTP header.

2. Providing your app's client id and secret via the `Client-ID` and `Client-Secret` HTTP headers. -This only works if your app is granted wider access to the api.-

# Formats

> To specify the data format:

```shell
curl "api_endpoint_here"
  -H "Authorization: theoauth2accesstoken"
  -H "Accepts: applicaiton/json"
  
curl "api_endpoint_here"
  -H "Authorization: theoauth2accesstoken"
  -H "Accepts: applicaiton/xml"  
```

The api will return `json` or `xml` based on the `Accepts` header. By default the api will return `json`.

The Ruby Gem will return an indifferent hash.
