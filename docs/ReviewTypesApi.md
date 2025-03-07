# Review Types Api

All URIs are relative to **SUBMISSION_API_URL** configuration variable.

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchReviewTypes**](ReviewTypesApi.md#searchReviewTypes) | **GET** /reviewTypes | Search review types.
[**headReviewTypes**](ReviewTypesApi.md#headReviewTypes) | **HEAD** /reviewTypes | Same to search review types, but only response status and headers information return.
[**createReviewType**](ReviewTypesApi.md#createReviewType) | **POST** /reviewTypes | Create a review type.
[**getReviewType**](ReviewTypesApi.md#getReviewType) | **GET** /reviewTypes/{reviewTypeId} | Get the review type.
[**headReviewType**](ReviewTypesApi.md#headReviewType) | **HEAD** /reviewTypes/{reviewTypeId} | Same to get review type, but only response status and headers information return.
[**updateReviewType**](ReviewTypesApi.md#updateReviewType) | **PUT** /reviewTypes/{reviewTypeId} | Fully update review type.
[**patchReviewType**](ReviewTypesApi.md#patchReviewType) | **PATCH** /reviewTypes/{reviewTypeId} | Partially update review type.
[**deleteReviewType**](ReviewTypesApi.md#deleteReviewType) | **DELETE** /reviewTypes/{reviewTypeId} | Delete the review type.

<a name="searchReviewTypes"></a>
# **searchReviewTypes**
> searchReviewTypes(reqQuery)

Search review types. Link headers are sent back and they have rel set to prev, next, first, last and contain the relevant URL.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reqQuery = {
  page: 1,
  perPage: 10,
  name: 'Review',
  isActive: true
}

// Promise model
submissionApiClient
  .searchReviewTypes(reqQuery)
  .then(result => console.log(result.body, result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.searchReviewTypes(reqQuery)
```

### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reqQuery** | [**Criteria**](Criteria.md)| the search criteria
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

Array of [**ReviewType**](ReviewType.md)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="headReviewTypes"></a>
# **headReviewTypes**
> headReviewTypes(reqQuery)

Same to search review types, but only response status and headers information return.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reqQuery = {
  page: 1,
  perPage: 10,
  name: 'Review',
  isActive: true
}

// Promise model
submissionApiClient
  .headReviewTypes(reqQuery)
  .then(result => console.log(result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.headReviewTypes(reqQuery)
```

### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reqQuery** | [**Criteria**](Criteria.md)| the search criteria
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

null (empty response body)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createReviewType"></a>
# **createReviewType**
> createReviewType(reqBody)

Create a review type.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reqBody = {
  name: 'Review',
  isActive: true
}

// Promise model
submissionApiClient
  .createReviewType(reqBody)
  .then(result => console.log(result.body, result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.createReviewType(reqBody)
```

### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reqBody** | [**ReviewTypeData**](ReviewTypeData.md)| the review type data
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

[**ReviewType**](ReviewType.md)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getReviewType"></a>
# **getReviewType**
> getReviewType(reviewTypeId)

Get the review type by id.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reviewTypeId = '8f4e8b6a-0ad2-4ff6-ab19-afeb102ff3b4'

// Promise model
submissionApiClient
  .getReviewType(reviewTypeId)
  .then(result => console.log(result.body, result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.getReviewType(reviewTypeId)
```
### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reviewTypeId** | String | the review type id
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

[**ReviewType**](ReviewType.md)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="headReviewType"></a>
# **headReviewType**
> headReviewType(reviewTypeId)

Same to get review type, but only response status and headers information return.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reviewTypeId = '8f4e8b6a-0ad2-4ff6-ab19-afeb102ff3b4'

// Promise model
submissionApiClient
  .headReviewType(reviewTypeId)
  .then(result => console.log(result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.headReviewType(reviewTypeId)
```

### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reviewTypeId** | String | the review type id
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

null (empty response body)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateReviewType"></a>
# **updateReviewType**
> updateReviewType(reviewTypeId, reqBody)

Fully update review type.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reviewTypeId = '8f4e8b6a-0ad2-4ff6-ab19-afeb102ff3b4'
const reqBody = {
  name: 'Review',
  isActive: true
}

// Promise model
submissionApiClient
  .updateReviewType(reviewTypeId, reqBody)
  .then(result => console.log(result.body, result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.updateReviewType(reviewTypeId, reqBody)
```

### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reviewTypeId** | String | the review type id
 **reqBody** | [**ReviewTypeData**](ReviewTypeData.md)| the review type data
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

[**ReviewType**](ReviewType.md)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="patchReviewType"></a>
# **patchReviewType**
> patchReviewType(reviewTypeId, reqBody)

Partially update review type.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reviewTypeId = '8f4e8b6a-0ad2-4ff6-ab19-afeb102ff3b4'
const reqBody = {
  name: 'Review',
  isActive: true
}

// Promise model
submissionApiClient
  .patchReviewType(reviewTypeId, reqBody)
  .then(result => console.log(result.body, result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.patchReviewType(reviewTypeId, reqBody)
```

### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reviewTypeId** | String | the review type id
 **reqBody** | [**ReviewTypeData**](ReviewTypeData.md)| the review type data
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

[**ReviewType**](ReviewType.md)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteReviewType"></a>
# **deleteReviewType**
> deleteReviewType(reviewTypeId)

Delete review type by id.

### Example
```javascript
const submissionApi = require('topcoder-submission-api-wrapper')
const submissionApiClient = submissionApi(_.pick(config,
      ['AUTH0_URL', 'AUTH0_AUDIENCE', 'TOKEN_CACHE_TIME',
        'AUTH0_CLIENT_ID', 'AUTH0_CLIENT_SECRET', 'SUBMISSION_API_URL',
        'AUTH0_PROXY_SERVER_URL']))

const reviewTypeId = '8f4e8b6a-0ad2-4ff6-ab19-afeb102ff3b4'

// Promise model
submissionApiClient
  .deleteReviewType(reviewTypeId)
  .then(result => console.log(result.status))
  .catch(err => console.log(err))

// Async / await model
await submissionApiClient.deleteReviewType(reviewTypeId)
```

### Parameters

Name | Type | Description
------------- | ------------- | -------------
 **reviewTypeId** | String | the review type id
 **userJwtToken** | String | User Authorization Token (Optional)
 
### Return type

null (empty response body)

### Authorization

[Bearer](../README.md#authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json
