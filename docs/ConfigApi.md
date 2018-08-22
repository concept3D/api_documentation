# AtlasBackendApi.ConfigApi

All URIs are relative to *https://dev.concept3d.com:8888*

Method | HTTP request | Description
------------- | ------------- | -------------
[**configGet**](ConfigApi.md#configGet) | **GET** /config | endpoint to return map configuration information


<a name="configGet"></a>
# **configGet**
> configGet(map, key)

endpoint to return map configuration information

This endpoint is used in the inital load of the map to provide key variables.  This included map types, available features, etc. 

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.ConfigApi();

var map = 1.2; // Number | This is your map ID assigned when your map was created

var key = "key_example"; // String | This is the API Access Key.  If you are unsure of this, contact your Client Success manager to assist you.


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.configGet(map, key, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map** | **Number**| This is your map ID assigned when your map was created | 
 **key** | **String**| This is the API Access Key.  If you are unsure of this, contact your Client Success manager to assist you. | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

