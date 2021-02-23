--- 

title: API Docs for ESL SaaS Server 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

Created by SoluM<br/>See more at https://solumesl.com/ 

**Version:** 1.0 

# Authentication 

|apiKey|*API Key*|
|---|---| 

# /V2/COMMON/LOGIN
## ***POST*** 

**Summary:** Login User

### HTTP Request 
`***POST*** /v2/common/login` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | Login Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | There is no account with the id |
| 401 | Password is expired |
| 402 | License is expired |
| 406 | Authentication Failed |
| 500 | Failed to process request operation |

# /V2/COMMON/FUNCTIONS/LED/PATTERN
## ***GET*** 

**Summary:** Get LED Patterns

### HTTP Request 
`***GET*** /v2/common/functions/led/pattern` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***POST*** 

**Summary:** Add LED Pattern

### HTTP Request 
`***POST*** /v2/common/functions/led/pattern` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Pattern Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***DELETE*** 

**Summary:** Delete LED Configuration

### HTTP Request 
`***DELETE*** /v2/common/functions/led/pattern` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| pattern | query | LED Pattern Name | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***PUT*** 

**Summary:** Update LED Pattern

### HTTP Request 
`***PUT*** /v2/common/functions/led/pattern` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| pattern | query | LED Pattern Name | Yes | string |
| requestMessage | body | Pattern Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCOUNT/DETAIL
## ***GET*** 

**Summary:** Get account info

**Description:** Get account info

### HTTP Request 
`***GET*** /v2/common/account/detail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| account | query | Account Name | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Data available |
| 500 | Failed to process request operation |

# /V2/COMMON/ACCESSLEVEL
## ***GET*** 

**Summary:** Get Levels Details

**Description:** This API supports  Sorting  Supported Sort Columns - <b>accessLevel </b> <br/>Supported Sort Orders - <b>asc and desc</b><br/>

### HTTP Request 
`***GET*** /v2/common/accessLevel` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| sort | query | Sort by accessLevel | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCESSLEVEL/TITLE
## ***PUT*** 

**Summary:** Update Level

### HTTP Request 
`***PUT*** /v2/common/accessLevel/title` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| accessLevel | query | Access Level | Yes | integer |
| requestMessage | body | Update Level Name | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCESSLEVEL/MENU
## ***PUT*** 

**Summary:** Update Menu Level Details

### HTTP Request 
`***PUT*** /v2/common/accessLevel/menu` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| accessLevel | query | Access Level | Yes | integer |
| requestMessage | body | Update Menu Level Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCESSLEVEL/ACTION
## ***PUT*** 

**Summary:** Update Action Access Details

### HTTP Request 
`***PUT*** /v2/common/accessLevel/action` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| accessLevel | query | Access Level | Yes | integer |
| requestMessage | body | Update Action Access Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCESSLEVEL/ONE
## ***GET*** 

**Summary:** Get Levels comes under accessLevel

### HTTP Request 
`***GET*** /v2/common/accessLevel/one` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| accessLevel | query | Access Level | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCESSLEVEL/MENU/RESET
## ***GET*** 

**Summary:** Get  Access Levvel Details after  Menu Reset

### HTTP Request 
`***GET*** /v2/common/accessLevel/menu/reset` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| accessLevel | query | Access Level | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCESSLEVEL/ACTION/RESET
## ***GET*** 

**Summary:** Get  Access Levvel Details after  Menu Reset

### HTTP Request 
`***GET*** /v2/common/accessLevel/action/reset` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| accessLevel | query | Access Level | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ACCOUNT/MAPPING
## ***POST*** 

**Summary:** Add account mapping

### HTTP Request 
`***POST*** /v2/common/account/mapping` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | Accounts Information which all comes under store | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***DELETE*** 

**Summary:** Delete account mapping

### HTTP Request 
`***DELETE*** /v2/common/account/mapping` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | Delete allowed permission regions | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/GATEWAY/DETAIL
## ***GET*** 

**Summary:** Get Gateway Configuration

### HTTP Request 
`***GET*** /v2/common/gateway/detail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| gateway | query | Gateway MacAddress | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/GATEWAY
## ***GET*** 

**Summary:** Get Gateways

**Description:** This API Supports Pagination & Sorting <br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/> Supported Sorting Columns - <b> ip, mac, version, labelCount </b><br/> Supported Network param - <b> online, offline </b>

### HTTP Request 
`***GET*** /v2/common/gateway` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| mac | query | gw macaddress | No | string |
| network | query | network | No | string |
| sort | query | Sort Params | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***POST*** 

**Summary:** Add Gateway

### HTTP Request 
`***POST*** /v2/common/gateway` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Gateway Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 409 | Store Already Exists |
| 500 | Failed to process request operation |

## ***PUT*** 

**Summary:** Update Gateway

### HTTP Request 
`***PUT*** /v2/common/gateway` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| gateway | query | Gateway MacAddress | Yes | string |
| requestMessage | body | Gateway Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***DELETE*** 

**Summary:** Delete Gateways

### HTTP Request 
`***DELETE*** /v2/common/gateway` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| gateways | query | Gateways MacAddress(seperator ,) | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***PATCH*** 

**Summary:** Reboot Gateway

### HTTP Request 
`***PATCH*** /v2/common/gateway` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| gateway | query | Gateway MacAddress | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/GATEWAY/FLOATING
## ***GET*** 

**Summary:** Get floating Gateways

### HTTP Request 
`***GET*** /v2/common/gateway/floating` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| mac | query | gw macaddress | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/DATA
## ***GET*** 

**Summary:** Get Supported Label Types

### HTTP Request 
`***GET*** /v2/common/templates/data` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES
## ***GET*** 

**Summary:** Get Templates

**Description:** This API Supports Pagination & Sorting <br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>templateName, lastUpdatedTime, labelType, width, height </b> <br/> Pagination Parameters - <b> page={currentPage}&size={rowsPerPage} </b>

### HTTP Request 
`***GET*** /v2/common/templates` 

**Parameters**

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

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***POST*** 

**Summary:** Add Templates

### HTTP Request 
`***POST*** /v2/common/templates` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Templates Body | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***DELETE*** 

**Summary:** Delete Templates

### HTTP Request 
`***DELETE*** /v2/common/templates` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Delete Template Body | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/NAME
## ***GET*** 

**Summary:** Get Templates By Name

**Description:** This API Sorting <br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>templateName, lastUpdatedTime, labelType, width, height </b>

### HTTP Request 
`***GET*** /v2/common/templates/name` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| name | query | Template Name | Yes | string |
| sort | query | Sort Params | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/LABEL/TYPE
## ***GET*** 

**Summary:** Get Templates By Label Type

**Description:** This API Sorting <br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>templateName, lastUpdatedTime, labelType, width, height </b>

### HTTP Request 
`***GET*** /v2/common/templates/label/type` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| labelType | query | Label Type | Yes | string |
| sort | query | Sort Params | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/HISTORY
## ***GET*** 

**Summary:** Get Template Update History

### HTTP Request 
`***GET*** /v2/common/templates/history` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| templateName | query | Template Name | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/DOWNLOAD
## ***GET*** 

**Summary:** Get Template Update History

### HTTP Request 
`***GET*** /v2/common/templates/download` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| templateName | query | Template Name | Yes | string |
| version | query | Version | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ARTICLES
## ***POST*** 

**Summary:** Add Articles

### HTTP Request 
`***POST*** /v2/common/articles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Article Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***PUT*** 

**Summary:** Update Articles

### HTTP Request 
`***PUT*** /v2/common/articles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Article Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***DELETE*** 

**Summary:** Delete Articles

### HTTP Request 
`***DELETE*** /v2/common/articles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Article Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Get Articles

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, articleName, nfcUrl, generateDate, lastUpdated </b>

### HTTP Request 
`***GET*** /v2/common/articles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| id | query | Article Id | No | string |
| name | query | Article Name | No | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |
| export | query | Export Status | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/UPLOAD/FORMAT
## ***POST*** 

**Summary:** Upload Article Data Format

### HTTP Request 
`***POST*** /v2/common/articles/upload/format` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | JSON format of article | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/ARTICLEFIELD
## ***GET*** 

**Summary:** Get Article Info

### HTTP Request 
`***GET*** /v2/common/config/articleField` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| article | query | Article Id | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/ARTICLEFIELDNSECONDLY
## ***GET*** 

**Summary:** Get Article Info By Id or Any Configured key value

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, articleName, nfcUrl, generateDate, lastUpdated </b>

### HTTP Request 
`***GET*** /v2/common/config/articleFieldNSecondly` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| article | query | Article Id or any configured key value | No | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/ARTICLE/INFO
## ***GET*** 

**Summary:** Get Article Info By Id or Article Name

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, articleName, nfcUrl, generateDate, lastUpdated </b>

### HTTP Request 
`***GET*** /v2/common/config/article/info` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| articleId | query | Article Id | No | string |
| articleName | query | Article Name | No | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/DATA
## ***GET*** 

**Summary:** Get Article Data Key List

### HTTP Request 
`***GET*** /v2/common/articles/data` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/ID
## ***GET*** 

**Summary:** Get Articles By Id

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, articleName, nfcUrl, generateDate, lastUpdated </b>

### HTTP Request 
`***GET*** /v2/common/articles/id` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| id | query | Article Id | Yes | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/IDNSECONDLY
## ***GET*** 

**Summary:** Get Articles By Id OR Any Configured Key based

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, articleName, nfcUrl, generateDate, lastUpdated </b>

### HTTP Request 
`***GET*** /v2/common/articles/idNSecondly` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| id | query | Article Id OR Any Configured Key Value | Yes | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/NAME
## ***GET*** 

**Summary:** Get Articles By Name

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, articleName, nfcUrl, generateDate, lastUpdated </b>

### HTTP Request 
`***GET*** /v2/common/articles/name` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| name | query | Article Name | Yes | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/NFC
## ***GET*** 

**Summary:** Get Articles By NFC Url

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, articleName, nfcUrl, generateDate, lastUpdated </b>

### HTTP Request 
`***GET*** /v2/common/articles/nfc` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| nfcUrl | query | NFC Url | Yes | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/UPLOAD
## ***POST*** 

**Summary:** Upload Articles Using File

### HTTP Request 
`***POST*** /v2/common/articles/upload` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | company code | Yes | string |
| store | query | Store Code | No | string |
| requestMessage | body | Article Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/LED
## ***PUT*** 

**Summary:** Blink Label LED By Article

### HTTP Request 
`***PUT*** /v2/common/articles/led` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Article & LED Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/UPDATE/HISTORY
## ***GET*** 

**Summary:** Get Article History

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>uploadDate </b>

### HTTP Request 
`***GET*** /v2/common/articles/update/history` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| article | query | Article Id | Yes | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/HISTORY
## ***GET*** 

**Summary:** Get Articles Update Batches

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>name, created </b><br/> Supported Search Columns - <b>name </b>

### HTTP Request 
`***GET*** /v2/common/articles/history` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | No | string |
| start | query | Start Date | No | string |
| end | query | End Date | No | string |
| name | query | file Name / Batch Name | No | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |
| export | query | Export Articles History Data. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/HISTORY/DETAIL
## ***GET*** 

**Summary:** Get Articles Update Batch Details

**Description:** This API supports Pagination, Sorting, Searching <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>articleId, labelCode, result, updateTime, errorCode </b><br/> Supported Search Columns - <b>articleId, labelCode, result, updateTime, errorCode </b>

### HTTP Request 
`***GET*** /v2/common/articles/history/detail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| name | query | Article Batch Id / CSV File Name | Yes | string |
| store | query | Store Code | No | string |
| articleId | query | Article Id | No | string |
| labelCode | query | Label Code | No | string |
| result | query | Result Status | No | string |
| errorCode | query | Error Code | No | string |
| sort | query | Sort Params | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/ARTICLES/MAP/RESERVED
## ***GET*** 

**Summary:** Get Reserved Assign Barcode Result

### HTTP Request 
`***GET*** /v2/common/articles/map/reserved` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/MAPPING/GROUP
## ***GET*** 

**Summary:** Get Template Groups

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>groupName, lastModifiedDate </b>

### HTTP Request 
`***GET*** /v2/common/templates/mapping/group` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| name | query | Group Name | No | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |
| sort | query | Sort Params | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***POST*** 

**Summary:** Add/Update Template Group

### HTTP Request 
`***POST*** /v2/common/templates/mapping/group` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Template Group Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***DELETE*** 

**Summary:** Delete Template Group

### HTTP Request 
`***DELETE*** /v2/common/templates/mapping/group` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Template Group Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***PUT*** 

**Summary:** Update Template Group

### HTTP Request 
`***PUT*** /v2/common/templates/mapping/group` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| group | query | Template Group Name | Yes | string |
| requestMessage | body | Template Group Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/MAPPING/GROUP/DETAIL
## ***GET*** 

**Summary:** Get Template List By Group

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>name </b>

### HTTP Request 
`***GET*** /v2/common/templates/mapping/group/detail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| group | query | Group Name | Yes | string |
| page | query | Page Number | No | string |
| size | query | Page Row Size | No | string |
| sort | query | Sort Params | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/MAPPING/CONDITION
## ***POST*** 

**Summary:** Add Template Mapping

### HTTP Request 
`***POST*** /v2/common/templates/mapping/condition` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| page | query | Page Number | Yes | string |
| requestMessage | body | Template Mapping Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***GET*** 

**Summary:** Get Template Mapping

### HTTP Request 
`***GET*** /v2/common/templates/mapping/condition` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| page | query | Page Number | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/MAPPING/CONDITION/COUNT
## ***GET*** 

**Summary:** Get Condition Page Count

### HTTP Request 
`***GET*** /v2/common/templates/mapping/condition/count` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/STORE
## ***POST*** 

**Summary:** Add Store

### HTTP Request 
`***POST*** /v2/common/store` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Store Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 409 | Store Already Exists |
| 500 | Failed to process request operation |

## ***PUT*** 

**Summary:** Update Store

### HTTP Request 
`***PUT*** /v2/common/store` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Store Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***DELETE*** 

**Summary:** Delete Store

### HTTP Request 
`***DELETE*** /v2/common/store` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Delete Store Codes | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Get Stores

**Description:** This API supports Pagination, Sorting & Searcing <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>store, storeName, region, country, labelCount, gatewayCount, lastUpdateTime </b> <br/> Supported Search Columns - <b>country={country}, region={region}, storeName={storeName}</b>

### HTTP Request 
`***GET*** /v2/common/store` 

**Parameters**

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

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/STORE/SUMMARY
## ***GET*** 

**Summary:** Get Store Summary

### HTTP Request 
`***GET*** /v2/common/store/summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/STORE/TIMEZONE
## ***GET*** 

**Summary:** GET Timezone List

### HTTP Request 
`***GET*** /v2/common/store/timezone` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/EMAILSETTING
## ***GET*** 

**Summary:** Get Email Server Changes

### HTTP Request 
`***GET*** /v2/common/config/emailsetting` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***PUT*** 

**Summary:** Update Email Server Changes

### HTTP Request 
`***PUT*** /v2/common/config/emailsetting` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Update Email Server Changes | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/FUNCTION
## ***GET*** 

**Summary:** Get Function Option Details

### HTTP Request 
`***GET*** /v2/common/config/function` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***POST*** 

**Summary:** Insert Function Options

### HTTP Request 
`***POST*** /v2/common/config/function` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Insert Function Options | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/ALIVEINTERVAL
## ***PUT*** 

**Summary:** Update Alive Interval

### HTTP Request 
`***PUT*** /v2/common/config/aliveInterval` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| aliveInterval | query | alive Interval Value | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Update Alive Interval

### HTTP Request 
`***GET*** /v2/common/config/aliveInterval` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/ALERTSETTING
## ***POST*** 

**Summary:** Insert Signal Setting Save Options

### HTTP Request 
`***POST*** /v2/common/config/alertsetting` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Insert Signal Setting Save Options | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Get Signal Setting Save Options

### HTTP Request 
`***GET*** /v2/common/config/alertsetting` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/AREA
## ***POST*** 

**Summary:** Insert area Setting

### HTTP Request 
`***POST*** /v2/common/area` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | Insert area Settings | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***PUT*** 

**Summary:** Update area Setting

### HTTP Request 
`***PUT*** /v2/common/area` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | Update area Settings | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Get Signal Setting Save Options

### HTTP Request 
`***GET*** /v2/common/area` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***DELETE*** 

**Summary:** delete area Setting

### HTTP Request 
`***DELETE*** /v2/common/area` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | delete area Settings | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/CONFIG/ASSIGNBARCODE
## ***POST*** 

**Summary:** Insert Assign Barcode

### HTTP Request 
`***POST*** /v2/common/config/assignbarcode` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Assign Barcode Request Body | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Get Assign Barcode

### HTTP Request 
`***GET*** /v2/common/config/assignbarcode` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LABELS/FORCE/ALIVE/SIGNAL
## ***PUT*** 

**Summary:** Send Force Alive Signal

### HTTP Request 
`***PUT*** /v2/common/labels/force/alive/signal` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Invalid input |
| 500 | Failed to process requested operation |

# /V2/COMMON/LABELS/RESEND/TIMEOUT
## ***PUT*** 

**Summary:** Resend Images for Timeout Labels

### HTTP Request 
`***PUT*** /v2/common/labels/resend/timeout` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Company Invalid |
| 405 | Invalid input |
| 500 | Failed to process requested operation |

# /V2/COMMON/LABELS/DETAIL
## ***GET*** 

**Summary:** Get Label Detail Image( previous/Current )

### HTTP Request 
`***GET*** /v2/common/labels/detail` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| label | query | Label Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LABELS
## ***GET*** 

**Summary:** Get Labels

### HTTP Request 
`***GET*** /v2/common/labels` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| label | query | Label Code | No | string |
| gateway | query | Gateway Mac | No | string |
| type | query | Model | No | string |
| status | query | Label Status | No | string |
| network | query | Network Status | No | string |
| battery | query | Battery Status | No | string |
| signal | query | Signal Status | No | string |
| template | query | Template | No | string |
| misusedLabelType | query | MisusedLabelType | No | string |
| sort | query | Sort Params | No | string |
| export | query | Export Status | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***DELETE*** 

**Summary:** Delete Labels

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>labelCode, articleId, articleName, gateway, network, battery</b><br/> status Parameters - <b>status={SUCCESS/PROCESSING/TIMEOUT}</b><br/> network Parameters - <b>network={online/offline}</b><br/> battery Parameters - <b>battery={good/bad}</b><br/> signal Parameters - <b>signal={excellent/good/bad}</b><br/> misusedLabelType Parameters - <b>misusedLabelType={all/normal/freezer}</b>

### HTTP Request 
`***DELETE*** /v2/common/labels` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Assign Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/LINK
## ***POST*** 

**Summary:** Assign Labels

### HTTP Request 
`***POST*** /v2/common/labels/link` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Assign Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Get Assign Info

### HTTP Request 
`***GET*** /v2/common/labels/link` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| labelCode | query | Label Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Data Available |
| 403 | Company Code Invalid |
| 405 | Invalid input |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/PAGE
## ***POST*** 

**Summary:** Change Display Page of Label

### HTTP Request 
`***POST*** /v2/common/labels/page` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Assign Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/LED
## ***PUT*** 

**Summary:** Blink Label LED by Label Code

### HTTP Request 
`***PUT*** /v2/common/labels/led` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Assign Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

## ***GET*** 

**Summary:** Get Labels LED Status

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>lastUpdated</b><br/> Supported Search Columns - <b>labelCode, startDate, endDate </b>

### HTTP Request 
`***GET*** /v2/common/labels/led` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| labelCode | query | Label Code | No | string |
| startDate | query | Start Date | No | string |
| endDate | query | End Date | No | string |
| sort | query | Sort Parameters | No | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Data Available |
| 403 | Company Invalid |
| 405 | Invalid input |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/UNLINK
## ***POST*** 

**Summary:** Unlink Labels & Articles

### HTTP Request 
`***POST*** /v2/common/labels/unlink` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Assign Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/TYPE/INFO
## ***GET*** 

**Summary:** Get ESL Label Type Information

### HTTP Request 
`***GET*** /v2/common/labels/type/info` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| labelCode | query | Label Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 405 | Invalid input |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/TYPE
## ***GET*** 

**Summary:** Get Supported Labels Type In Store

### HTTP Request 
`***GET*** /v2/common/labels/type` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Company Invalid |
| 405 | Invalid input |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/HISTORY
## ***GET*** 

**Summary:** Get ESL Label History

### HTTP Request 
`***GET*** /v2/common/labels/history` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| label | query | Label Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 405 | Invalid input |
| 500 | Failed to process request operation |

# /V2/COMMON/TEMPLATES/MAPPING/CONDITION/APPLY
## ***PUT*** 

**Summary:** Update apply conditions

### HTTP Request 
`***PUT*** /v2/common/templates/mapping/condition/apply` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Apply Conditions Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/TEMPLATES/MAPPING/CONDITION/APPLY/GENERATE
## ***PUT*** 

**Summary:** Apply Template Mapping Based on Schedule

### HTTP Request 
`***PUT*** /v2/common/templates/mapping/condition/apply/generate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/CONFIG/REPORT
## ***POST*** 

**Summary:** Add Report Settings Details

### HTTP Request 
`***POST*** /v2/common/config/report` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | Report Settings Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***GET*** 

**Summary:** Get Report Settings Details

### HTTP Request 
`***GET*** /v2/common/config/report` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LABELS/IMAGE
## ***POST*** 

**Summary:** Image Push By Label

### HTTP Request 
`***POST*** /v2/common/labels/image` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Image Push Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/COMPANY
## ***GET*** 

**Summary:** Get Company Details

### HTTP Request 
`***GET*** /v2/common/company` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company code | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Customers available |
| 500 | Failed to process request operation |

## ***POST*** 

**Summary:** Create Company

### HTTP Request 
`***POST*** /v2/common/company` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| requestMessage | body | Company data to create | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Company Created |
| 400 | Invalid input |
| 409 | Duplicate(Company Already Exists) |
| 500 | Failed to process request operation |

## ***PUT*** 

**Summary:** Update Company

### HTTP Request 
`***PUT*** /v2/common/company` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company code | Yes | string |
| requestMessage | body | Company data to update | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Company Updated |
| 400 | Invalid input |
| 500 | Failed to process request operation |

# /V2/COMMON/SUMMARY
## ***GET*** 

**Summary:** total store summary

### HTTP Request 
`***GET*** /v2/common/summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| account | query | User Account Name | Yes | string |
| store | query | Store Code | No | string |
| country | query | Country | No | string |
| region | query | Region | No | string |
| city | query | city | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/SUMMARY/PROBLEM
## ***GET*** 

**Summary:** store problem summary

**Description:** problemType Parameters - <b>problemType={problemType}</b><br/>Supported Problem Type - <b>updateFailure, labelOffline, lowBattery, badSignal, misused, gatewayOffline</b>

### HTTP Request 
`***GET*** /v2/common/summary/problem` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| account | query | User Account Name | No | string |
| store | query | Store Code | No | string |
| country | query | Country | No | string |
| region | query | Region | No | string |
| problemType | query | problemType | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LICENSE
## ***GET*** 

**Summary:** Get License Details

### HTTP Request 
`***GET*** /v2/common/license` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Company Invalid |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/ABOUT
## ***GET*** 

**Summary:** API Service Info

### HTTP Request 
`***GET*** /v2/common/about` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 500 | Failed to process request operation |

# /V2/COMMON/VERSION
## ***GET*** 

**Summary:** Get all Services version Info

### HTTP Request 
`***GET*** /v2/common/version` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 500 | Failed to process request operation |

# /V2/COMMON/LABELS/SCHEDULE
## ***POST*** 

**Summary:** Post Schedules for Labels

### HTTP Request 
`***POST*** /v2/common/labels/schedule` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***GET*** 

**Summary:** Get Labels Schedule Info

### HTTP Request 
`***GET*** /v2/common/labels/schedule` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| label | query | Label Code | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LABELS/SCHEDULE/ARTICLE
## ***POST*** 

**Summary:** Post Schedules for Articles

### HTTP Request 
`***POST*** /v2/common/labels/schedule/article` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| store | query | Store Code | Yes | string |
| requestMessage | body | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/ANCHOR/CONFIG
## ***GET*** 

**Summary:** Get LBS Anchor Config

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, requestDate </b>

### HTTP Request 
`***GET*** /v2/common/lbs/anchor/config` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***POST*** 

**Summary:** Add LBS Anchor Config

### HTTP Request 
`***POST*** /v2/common/lbs/anchor/config` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| requestMessage | body | LBS Anchor Config Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/ANCHOR/CONFIG/GETBYLABEL/{LABELID}
## ***GET*** 

**Summary:** Get LBS Anchor Config by Label

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, requestDate </b>

### HTTP Request 
`***GET*** /v2/common/lbs/anchor/config/getByLabel/{labelId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| labelId | path | Label Id | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/ANCHOR/CONFIG/GETBYSTORE/{STOREID}
## ***GET*** 

**Summary:** Get LBS Anchor Config by Store

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, requestDate </b>

### HTTP Request 
`***GET*** /v2/common/lbs/anchor/config/getByStore/{storeId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| storeId | path | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/ANCHOR/CONFIG/GETBYPOSITION/{POSITIONID}
## ***GET*** 

**Summary:** Get LBS Anchor Config by Position

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, requestDate </b>

### HTTP Request 
`***GET*** /v2/common/lbs/anchor/config/getByPosition/{positionId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| positionId | path | Position Id | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/ANCHOR/CONFIG/GETBYARTICLEID/{ARTICLEID}
## ***GET*** 

**Summary:** Get LBS Anchor Config by Article

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeId, articleId, labelCode </b>

### HTTP Request 
`***GET*** /v2/common/lbs/anchor/config/getByArticleId/{articleId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| articleId | path | Article Id | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/ANCHOR/CONFIG/GETBYARTICLENAME/{ARTICLENAME}
## ***GET*** 

**Summary:** Get LBS Anchor Config by Article Name

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, labelCode, articleName </b>

### HTTP Request 
`***GET*** /v2/common/lbs/anchor/config/getByArticleName/{articleName}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| articleName | path | Article Name | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/ANCHOR/CONFIG/{LABELID}
## ***DELETE*** 

**Summary:** Delete LBS Anchor Config

### HTTP Request 
`***DELETE*** /v2/common/lbs/anchor/config/{labelId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| labelId | path | Label Id | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/CONFIG
## ***GET*** 

**Summary:** Get LBS Config

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, startTime, endTime, requestDate </b>

### HTTP Request 
`***GET*** /v2/common/lbs/config` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/CONFIG/{STOREID}
## ***DELETE*** 

**Summary:** Delete LBS Anchor Config

### HTTP Request 
`***DELETE*** /v2/common/lbs/config/{storeId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| storeId | path | Store Id | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***GET*** 

**Summary:** Get LBS Config By Store

### HTTP Request 
`***GET*** /v2/common/lbs/config/{storeId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| storeId | path | Store Id | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

## ***POST*** 

**Summary:** Add LBS Config

### HTTP Request 
`***POST*** /v2/common/lbs/config/{storeId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| storeId | path | Store Id | Yes | string |
| requestMessage | body | LBS Config Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

## ***PUT*** 

**Summary:** Update LBS Config

### HTTP Request 
`***PUT*** /v2/common/lbs/config/{storeId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| storeId | path | Store Id | Yes | string |
| requestMessage | body | LBS Config Info | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 405 | Parameter is invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/RESULT
## ***GET*** 

**Summary:** Get LBS Result

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, anchorUpdateTime, lbsUpdateTime </b>

### HTTP Request 
`***GET*** /v2/common/lbs/result` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/RESULT/GETBYSTORE/{STOREID}
## ***GET*** 

**Summary:** Get LBS Result by Store

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, anchorUpdateTime, lbsUpdateTime </b>

### HTTP Request 
`***GET*** /v2/common/lbs/result/getByStore/{storeId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| storeId | path | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/RESULT/GETBYPOSITION/{POSITIONID}
## ***GET*** 

**Summary:** Get LBS Result by Position

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, anchorUpdateTime, lbsUpdateTime </b>

### HTTP Request 
`***GET*** /v2/common/lbs/result/getByPosition/{positionId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| positionId | path | Position Id | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/RESULT/GETBYARTICLEID/{ARTICLEID}
## ***GET*** 

**Summary:** Get LBS Result by Article

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeId, articleId, labelCode </b>

### HTTP Request 
`***GET*** /v2/common/lbs/result/getByArticleId/{articleId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| articleId | path | Article Id | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/RESULT/GETBYARTICLENAME/{ARTICLENAME}
## ***GET*** 

**Summary:** Get LBS Result by Article Name

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, labelCode, articleName </b>

### HTTP Request 
`***GET*** /v2/common/lbs/result/getByArticleName/{articleName}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| articleName | path | Article Name | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

# /V2/COMMON/LBS/RESULT/GETBYLABEL/{LABELCODE}
## ***GET*** 

**Summary:** Get LBS Result by Label

**Description:** This API supports Pagination, Sorting <br/> Pagination Parameters - <b>page={currentPage}&size={rowsPerPage}</b><br/> Sort Parameters - <b>sort={sortColumn,sortOrder}</b><br/>Supported Sort Orders - <b>asc and desc</b><br/> Supported Sort Columns - <b>storeCode, positionId, labelCode, anchorUpdateTime, lbsUpdateTime </b>

### HTTP Request 
`***GET*** /v2/common/lbs/result/getByLabel/{labelCode}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| company | query | Company Code | Yes | string |
| labelCode | path | Label Code | Yes | string |
| storeId | query | Store Id | Yes | string |
| page | query | Page Number | No | integer |
| size | query | Page Row Size | No | integer |
| sort | query | Sort Parameters | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 204 | No Content |
| 403 | Company Invalid |
| 500 | Internal Server Error |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
