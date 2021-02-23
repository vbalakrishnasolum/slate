---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - Curl

toc_footers:
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true
---

<!-- Introudction Start  -->

# Introduction

Welcome to the ESL SaaS Server API! You can use our API to access ESL SaaS Server, which can get information on Labels, Gateways, Articles and many more.

We have language bindings in Shell. You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

<!-- Introudction End  -->

<!-- Authentication Start  -->
# Authentication

> To authorize, you need to generate the token using Azure AD B2C:

> Curl Example

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: Bearer generatedToken"
```

> Make sure to replace `generatedToken` with your Azure AD B2C token.

ESL SaaS Server uses token to allow access to the API.
You can register your email at provided ESL SaaS Server.

ESL SaaS Server expects for the token to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer generatedToken`

<aside class="notice">
You must replace <code>generatedToken</code> with your personal Azure AD B2C token.
</aside>

<!-- Authentication End  -->

<!-- Overview Start  -->

# Overview
This section of APIs will explain about SaaS Server Status and Version Information

## About
This endpoint shows the status of SaaS Server and memory related informationstatus

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'http://localhost.com/api/v2/common/about'

```

> Response Body

```json
{
  "type": "ESL Cloud",
  "description": "Integrate ESL Process Using APIs Provided by API Service",
  "instanceId": "2871969d-580d-411e-b51a-79f9b4f4b374",
  "version": "1.0.0",
  "nVersion": "v14.15.1",
  "hostname": "localhost",
  "memorySizeLimit": "4144.00 MB",
  "memorySizeLimitInBytes": 4345298944,
  "timeInfo": {
    "uptime": "16 secs",
    "systemTime": "2021-02-19 21:33:11",
    "timezone": "GMT+0530",
    "timezoneName": "Asia/Calcutta"
  },
  "memoryInfo": {
    "rss": "100 MB",
    "heapTotal": "50 MB",
    "heapUsed": "48 MB",
    "external": "22 MB"
  },
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}

```

### HTTP Request
<aside class="api">
GET /api/v2/common/about
</aside>

### Parameters

| Name | Located in | Description | Required
| ---- | ---------- | ----------- | --------

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 500 | Failed to process request operation |


## Version
This endpoint shows version SaaS Server

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://stage00.common.solumesl.com/common/api/v2/common/version'

```

> Response Body

```json

{
  "baseVersion": "1.0.1",
  "dashboard": {
    "name": "Dashboard",
    "version": "1.0.1.649"
  },
  "apiService": {
    "name": "API Service",
    "version": "1.0.1.930"
  },
  "ig": {
    "name": "ImageGenerator",
    "version": "1.0.1.820"
  },
  "inbound": {
    "name": "Inbound",
    "version": "1.0.1.925"
  },
  "outbound": {
    "name": "Outbound",
    "version": "1.0.1.771"
  },
  "pda": {
    "name": "PDA",
    "version": "1.0.1.421"
  },
  "scheduler": {
    "name": "Scheduler",
    "version": "1.0.1.905"
  },
  "layoutDesigner": {
    "name": "Layout Designer",
    "version": "1.0.1.689"
  },
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}

```

### HTTP Request

<aside class="api">
GET /api/v2/common/version
</aside>

### Parameters

| Name | Located in | Description | Required
| ---- | ---------- | ----------- | --------

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 500 | Failed to process request operation |

<!-- Overview End  -->

<!-- Stores Start -->

# Stores
This section of APIs will explain about how to create store, edit, delete stores and get stores

## Add
This endpoint shows how to add a store

> Curl Example

```shell
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' -d '{
   "region":"Karnataka",
   "city":"Bangalore",
   "storeName":"Hebbal Outlet",
   "store":"XHR231",
   "zoneId":"Asia/Kolkata",
   "ipNtpServer":null,
   "whiteListEnable":false,
   "lbsEnabled":false,
   "storeConfig":{
      "lostTime":"0",
      "logoDisplayTime":"0",
      "beaconLossLimit":"10",
      "aliveInterval":"24",
      "reactivationRetryLimit":"2",
      "scanPeriodSet":"0",
      "batteryMode":0,
      "location":0,
      "updatePageUnlock":false,
      "aesEnable":false,
      "acsEnable":false,
      "tapGoStartTime":"9",
      "tapGoEndTime":"21",
      "flexibleDefault":"0"
   }' 'http://localhost.com/api/v2/common/store?company=DEVTEST'
```

> Request Body

```json
{
   "company":"DEVTEST",
   "country":"India",
   "region":"Karnataka",
   "city":"Bangalore",
   "storeName":"Hebbal Outlet",
   "store":"XHR231",
   "zoneId":"Asia/Kolkata",
   "ipNtpServer":null,
   "whiteListEnable":false,
   "lbsEnabled":false,
   "storeConfig":{
      "lostTime":"0",
      "logoDisplayTime":"0",
      "beaconLossLimit":"10",
      "aliveInterval":"24",
      "reactivationRetryLimit":"2",
      "scanPeriodSet":"0",
      "batteryMode":0,
      "location":0,
      "updatePageUnlock":false,
      "aesEnable":false,
      "acsEnable":false,
      "tapGoStartTime":"9",
      "tapGoEndTime":"21",
      "flexibleDefault":"0"
   }
}

```

> Response Body

```json
{
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
POST /api/v2/common/store
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Store Info | Yes |  |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 409 | Store Already Exists |
| 500 | Failed to process request operation |

## Update
This endpoint shows how to update or edit store information

> Curl Example

```shell
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' -d '{
   "country":"India",
   "region":"Karnataka",
   "city":"Bangalore",
   "storeName":"Hebbal Outlet",
   "store":"XHR231",
   "zoneId":"Asia/Kolkata",
   "ipNtpServer":null,
   "whiteListEnable":false,
   "lbsEnabled":false,
   "storeConfig":{
      "lostTime":"0",
      "logoDisplayTime":"0",
      "beaconLossLimit":"10",
      "aliveInterval":"24",
      "reactivationRetryLimit":"2",
      "scanPeriodSet":"0",
      "batteryMode":0,
      "location":0,
      "updatePageUnlock":false,
      "aesEnable":false,
      "acsEnable":false,
      "tapGoStartTime":"9",
      "tapGoEndTime":"21",
      "flexibleDefault":"0"
   }' 'http://localhost.com/api/v2/common/store?company=DEVTEST&store=XHR231'
```

> Request Body

```json
{
   "country":"India",
   "region":"Karnataka",
   "city":"Bangalore",
   "storeName":"Hebbal Outlet",
   "zoneId":"Asia/Kolkata",
   "ipNtpServer":null,
   "whiteListEnable":false,
   "lbsEnabled":false,
   "storeConfig":{
      "lostTime":"0",
      "logoDisplayTime":"0",
      "beaconLossLimit":"10",
      "aliveInterval":"24",
      "reactivationRetryLimit":"2",
      "scanPeriodSet":"0",
      "batteryMode":0,
      "location":0,
      "updatePageUnlock":false,
      "aesEnable":false,
      "acsEnable":false,
      "tapGoStartTime":"9",
      "tapGoEndTime":"21",
      "flexibleDefault":"0"
   }
}

```

> Response Body

```json
{
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
PUT /api/v2/common/store
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Store Info | Yes |  |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## Delete
This endpoint shows how to delete a store

> Curl Example

```shell
curl -X DELETE --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}'  -d '{
  "storeList": [
    "XHR123"
  ]
}' 'http://localhost:8080/api/v2/common/store?company=DEVTEST'
```

> Request Body

```json
{
  "storeList": [
    "XHR123"
  ]
}

```

> Response Body

```json
{
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
DELETE /api/v2/common/store
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Delete Store Codes | Yes |  |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |


## Get Stores
This endpoint shows how to get the available list of stores

### Description:
This API supports Pagination, Sorting & Searcing <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>store, storeName, region, country, labelCount, gatewayCount, lastUpdateTime </b> <br/> Supported Search Columns - <b>country={country}, region={region}, storeName={storeName}</b>

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://stage00.common.solumesl.com/common/api/v2/common/store?company=DOUGLAS&export=false'

```


> Response Body

```json
{
  "stores": [
    {
      "lastUpdateTime": "2021-02-09 08:18:36.57338",
      "store": "XHR123",
      "storeName": "Hebbal Outlet",
      "region": "Karnataka",
      "city": "Bangalore",
      "company": "DEVTEST",
      "country": "India",
      "labelCount": 100,
      "gatewayCount": 2,
      "address": null,
      "zoneId": "Asia/Kolkata"
    }
  ],
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
GET /v2/common/store
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| account | query | User Account Name | No | string |
| store | query | Store Code | No | string |
| country | query | Country | No | string |
| region | query | Region | No | string |
| city | query | city | No | string |
| storeName | query | Store Name | No | string |
| isLoginResponse | query | Send True or False to keep the same response as login | No | boolean |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |
| export | query | Export Status | No | string |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Failed to process request operation |


## Summary
This endpoint shows information about store statistics like article, label, low battery, bad signal counts and more information

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://stage00.common.solumesl.com/common/api/v2/common/store/summary?company=DEVTEST&store=XHR123'

```


> Response Body

```json
{
  "address": "Hebbal",
  "city": "Bangalore",
  "country": "India",
  "region": "Karantaka",
  "store": "XHR123",
  "storeName": "Hebbal Outlet",
  "zoneId": "Asia/Kolkata",
  "ipNtpServer": null,
  "whiteListEnable": false,
  "lbsEnabled": true,
  "storeConfig": {
    "aliveInterval": 24,
    "lostTime": 0,
    "logoDisplayTime": 0,
    "beaconLossLimit": 0,
    "reactivationRetryLimit": 0,
    "scanPeriodSet": 0,
    "batteryMode": 0,
    "location": 0,
    "aesEnable": false,
    "acsEnable": false,
    "tapGoStartTime": 0,
    "tapGoEndTime": 0,
    "flexibleDefault": 0,
    "rebootRetryCount": 0,
    "updatePageUnlock": false
  },
  "company": "DEVTEST",
  "updatedLabelCount": 4,
  "inProgressLabelCount": 0,
  "notUpdatedLabelCount": 0,
  "totalUpdatedLabelCount": 4,
  "totalLabelCount": 4,
  "goodBatteryCount": 0,
  "lowBatteryCount": 0,
  "onlineLabelCount": 0,
  "offlineLabelCount": 0,
  "excellentSignalLabelCount": 0,
  "goodSignalLabelCount": 0,
  "badSignalLabelCount": 0,
  "onlineGwCount": 3,
  "notReadyGwCount": 0,
  "offlineGwCount": 0,
  "totalAssignedProductCount": 4,
  "totalProductCount": 12,
  "misUsedLabelCount": 0,
  "responseCode": "200",
  "responseMessage": "OK"
}
```


### HTTP Request

<aside class="api">
GET /v2/common/store/summary
</aside>


### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |


## Timezones
This endpoint gives information about available timezones

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://stage00.common.solumesl.com/common/api/v2/common/store/timezone'

```

> Response Body

```json
{
  "timezoneList": [
    {
      "name": "Africa/Abidjan",
      "timezone": "GMT"
    },
    {
      "name": "Africa/Addis_Ababa",
      "timezone": "GMT+03:00"
    },
    {
      "name": "Africa/Cairo",
      "timezone": "GMT+02:00"
    }
  ],
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
GET /v2/common/store/timezone
</aside>

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 500 | Failed to process request operation |

<!-- Stores End -->


<!-- Templates Start -->

# Templates
This section of APIs will explain about how to upload and view templates

## Add or Update
This endpoint shows how to upload a template

> Curl Example

```shell
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' -d '{
  "data": "PD94bWwgdmVyc2lvbj0iMS....",
  "templateName": "2P-Weiss",
  "labelType": "N_1_6",
  "fileType": "xsl",
  "width": "200",
  "height": "200",
  "tagImageUpdateRequired": false
}' 'http://localhost.com/api/v2/common/templates?company=DEVTEST'
```

> Request Body

```json
{
  "data": "PD94bWwgdmVyc2lvbj0iMS....",
  "templateName": "2P-Weiss",
  "labelType": "N_1_6",
  "fileType": "xsl",
  "width": "200",
  "height": "200",
  "tagImageUpdateRequired": false
}
```

> Response Body

```json
{
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
POST /v2/common/templates
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Templates Body | Yes |  |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |


## Delete
This endpoint shows how to delete template

> Curl Example

```shell
curl -X DELETE --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' -d '{
  "templateDeleteList": [
    "2P-Weiss"
  ]
}' 'http://localhost.com/api/v2/common/templates?company=DEVTEST'
```

> Request Body

```json
{
  "templateDeleteList": [
    "2P-Weiss"
  ]
}
```

> Response Body

```json
{
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
DELETE /v2/common/templates
</aside>


### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Delete Template Body | Yes |  |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |


## Get Templates
This endpoint shows how to get the available templates in server

### Description
This API Supports Searching, Pagination & Sorting
<br/>Search Columns - <b>width</b>, <b>height</b>, <b>labelCode</b>
<br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b>
<br/> Supported Sort Columns - <b>templateName, lastUpdatedTime, labelType, width, height </b> <br/> Pagination Parameters - <b> page={currentPage}&size={rowsPerPage} </b>

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://eu.common.solumesl.com/common/api/v2/common/templates?company=DOU&export=false'

```

> Response Body

```json
{
  "templateList": [
    {
      "templateName": "2GP-Schwarz",
      "labelType": "N_1_6",
      "width": 200,
      "height": 200,
      "lastUpdatedTime": "2021-02-18 11:20:19.862513",
      "version": 1
    },
    {
      "templateName": "2GP-Weiss",
      "labelType": "N_1_6",
      "width": 200,
      "height": 200,
      "lastUpdatedTime": "2021-02-18 11:19:54.939028",
      "version": 1
    }
  ],
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
GET /v2/common/templates
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| width | query | Width of template | No | string |
| height | query | Height of template | No | string |
| labelCode | query | Label Code | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |
| sort | query | Sort Params | No | string |
| export | query | Export Status | No | string |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |


## Supported Label Types
This endpoint shows how many label types supported

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://eu.common.solumesl.com/common/api/v2/common/templates/data?company=DOU'

```

> Request Body

```json
{
  "tagTypeList": [
    {
      "name": "N_1_6",
      "width": 200,
      "height": 200
    },
    {
      "name": "N_2_2",
      "width": 296,
      "height": 160
    }
  ],
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
GET /api/v2/common/templates/data
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## Template By Name
This endpoint shows how to get template by its name

### Description
This API Supports Sorting <br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>templateName, lastUpdatedTime, labelType, width, height </b>

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://eu.common.solumesl.com/common/api/v2/common/templates/name?company=DOU&name=2GP-Schwarz'

```

> Response Body

```json
{
  "templateList": [
    {
      "templateName": "2GP-Schwarz",
      "labelType": "N_1_6",
      "width": 200,
      "height": 200,
      "lastUpdatedTime": "2021-02-18 11:20:19.862513",
      "version": 1
    }
  ],
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
GET /api/v2/common/templates/name
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| name | query | Template Name | Yes | string |
| sort | query | Sort Params | No | string |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |


## History
This endpoint shows how to view the template history by name

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://eu.common.solumesl.com/common/api/v2/common/templates/history?company=DOU&templateName=2GP-Schwarz'

```

> Response Body

```json
{
  "templateHistoryList": [
    {
      "templateName": "2GP-Schwarz",
      "lastUpdateTime": "2021-02-18 11:20:19.926",
      "version": 1
    }
  ],
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
GET /api/v2/common/templates/history
</aside>


### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| templateName | query | Template Name | Yes | string |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |


## Templates By Label Type
This endpoint show to get the templates based on label type

### Description
This API Supports Sorting <br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>templateName, lastUpdatedTime, labelType, width, height </b>

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://eu.common.solumesl.com/common/api/v2/common/templates/label/type?company=DOU&labelType=0394B801B29C'

```

> Request Body

```json
{
  "templateList": [
    {
      "templateName": "2GP-Schwarz",
      "labelType": "N_1_6",
      "width": 200,
      "height": 200,
      "lastUpdatedTime": "2021-02-18 11:20:19.862513",
      "version": 1
    }
  ],
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class="api">
GET /api/v2/common/templates/label/type
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| labelType | query | Label Type | Yes | string |
| sort | query | Sort Params | No | string |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |


## Download
This endpoint shows how to download template

> Curl Example

```shell
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' 'https://eu.common.solumesl.com/common/api/v2/common/templates/download?company=DOU&templateName=2GP-Schwarz&version=1'

```

> Response Body

```json
{
  "template": "PD94bWwgdmVyc2lvbj0iMS4w...",
  "responseCode": "200",
  "responseMessage": "SUCCESS"
}
```

### HTTP Request

<aside class='api'>
GET /v2/common/templates/download
</aside>

### Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| templateName | query | Template Name | Yes | string |
| version | query | Version | Yes | integer |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

<!-- Templates End -->

# Template Mapping
This section of APIs will explain about how to manage template mapping and apply

# Products
This section of APIs will explain about products update, view, delete etc

# Gateways
This section of APIs will explain about how to register gateway, view gateways, reboot and delete gateways

# Labels
This section of APIs will explain about how to assign, unassign, led, schedule, view label status, image preview etc

# LED Pattern
This section of APIs will explain about how to change the LED patterns.

# Summary
This section of APIs will explain about summary of Label status etc

# User Management

This section of APIs will explain about user login, user levels, user & store mapping.

<!-- <aside class="success">
Login
</aside> -->

## Login

This endpoint is for login.

> Curl Example

```shell
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: Bearer {generatedToken}' -d '{
  "account": "username",
  "password": "password"
}' 'https://stage00.common.solumesl.com/common/api/v2/common/login'
```

> Request Body

```json
{
  "username":"admin",
  "password":"admin123"
}

```

> Response Body

```json
{
  "company": [
    "DEVTEST"
  ],
  "account": "7786bad8-308e-41a5-a0cd-218a284fca1a",
  "firstName": "SoluM Admin",
  "accountGroup": "Admin",
  "accountInfo": {
    "accessMenu": [
      "1000",
      "2000"
    ],
    "accessAction": [
      "1000",
      "2000"
    ],
    "accessLevel": 1,
    "title": "Admin"
  },
  "managedStores": [
    {
      "company": "DEVTEST",
      "country": "India",
      "region": "Karnataka",
      "city": "Bangalore",
      "code": "XHR123",
      "name": "Hebbal Outlet"
    }
  ],
  "aliveInterval": "24",
  "responseCode": "200",
  "responseMessage": "SUCCESS",
  "isSolumAdmin": true
}
```

### HTTP Request

`POST /v2/common/login`

### Query Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | Login Info | Yes |  |

### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | There is no account with the id |
| 401 | Password is expired |
| 402 | License is expired |
| 406 | Authentication Failed |
| 500 | Failed to process request operation |

# Audit Logs
This section of APIs will explain about how to view user audit logs etc

# System Configuration
This section of APIs will explain about how to do different configuration like Areas, email, alerts and report configuration

# License
This section of APIs will explain about license