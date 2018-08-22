# AtlasBackendApi.StylesApi

All URIs are relative to *https://dev.concept3d.com:8888*

Method | HTTP request | Description
------------- | ------------- | -------------
[**stylesGet**](StylesApi.md#stylesGet) | **GET** /styles | styles API returns CSS for Styles from CMS


<a name="stylesGet"></a>
# **stylesGet**
> stylesGet(map, key)

styles API returns CSS for Styles from CMS

the endpoint will return css for Version 2.0 of front end.  may not have relevance for other implementations.

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.StylesApi();

var map = 1.2; // Number | mapId

var key = "key_example"; // String | access key


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.stylesGet(map, key, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map** | **Number**| mapId | 
 **key** | **String**| access key | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

