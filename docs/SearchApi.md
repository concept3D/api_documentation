# AtlasBackendApi.SearchApi

All URIs are relative to *https://dev.concept3d.com:8888*

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchGet**](SearchApi.md#searchGet) | **GET** /search | search summary


<a name="searchGet"></a>
# **searchGet**
> searchGet(map, key, q, opts)

search summary

search description

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.SearchApi();

var map = 1.2; // Number | mapId

var key = "key_example"; // String | access key

var q = "q_example"; // String | string to search for

var opts = { 
  'page': 56, // Number | page number of search results
  'ppage': 56 // Number | results per page
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.searchGet(map, key, q, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map** | **Number**| mapId | 
 **key** | **String**| access key | 
 **q** | **String**| string to search for | 
 **page** | **Number**| page number of search results | [optional] 
 **ppage** | **Number**| results per page | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

