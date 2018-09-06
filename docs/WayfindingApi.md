# AtlasBackendApi.WayfindingApi

All URIs are relative to *https://dev.concept3d.com:8888*

Method | HTTP request | Description
------------- | ------------- | -------------
[**wayfindingGet**](WayfindingApi.md#wayfindingGet) | **GET** /wayfinding | search summary


<a name="wayfindingGet"></a>
# **wayfindingGet**
> wayfindingGet(map, key, opts)

get a Wayfinding route using data from concept3D CMS

Using a latitude/longitude for starting and ending points, find the preferred, quickest route to the destination.

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.WayfindingApi();

var map = 1.2; // Number | this is the map id you are requesting access for

var key = "key_example"; // String | This is a client specific key granting access to the data for the MAP ID above

var opts = { 
  'fromLat': 1.2, // Number | Latitude to start from
  'fromLng': 1.2, // Number | Longitude to start from
  'toLat': 1.2, // Number | Latitude to go to
  'toLng': 1.2, // Number | Longitude to go to
  'fromLevel': 56, // Number | Floor Level to start From (default is 0 - ground)
  'toLevel': 56, // Number | Floor level to go to (default is 0 - ground)
  'currentLevel': 56 // Number | Floor level you are currently on (default is 0 - ground)
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.wayfindingGet(map, key, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map** | **Number**| this is the map id you are requesting access for | 
 **key** | **String**| This is a client specific key granting access to the data for the MAP ID above | 
 **fromLat** | **Number**| Latitude to start from | [optional] 
 **fromLng** | **Number**| Longitude to start from | [optional] 
 **toLat** | **Number**| Latitude to go to | [optional] 
 **toLng** | **Number**| Longitude to go to | [optional] 
 **fromLevel** | **Number**| Floor Level to start From (default is 0 - ground) | [optional] 
 **toLevel** | **Number**| Floor level to go to (default is 0 - ground) | [optional] 
 **currentLevel** | **Number**| Floor level you are currently on (default is 0 - ground) | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

