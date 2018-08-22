# AtlasBackendApi.LocationsApi

All URIs are relative to *https://dev.concept3d.com:8888*

Method | HTTP request | Description
------------- | ------------- | -------------
[**locationsGet**](LocationsApi.md#locationsGet) | **GET** /locations | Locations Endpoint.  Does not use a location ID
[**locationsLocationIdGet**](LocationsApi.md#locationsLocationIdGet) | **GET** /locations/{locationId} | locations summary


<a name="locationsGet"></a>
# **locationsGet**
> locationsGet(map, key, ref)

Locations Endpoint.  Does not use a location ID

Location API is used to retrieve data regarding a location

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.LocationsApi();

var map = 1.2; // Number | The Map Id you are querying

var key = "key_example"; // String | access key

var ref = "ref_example"; // String | ref id


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.locationsGet(map, key, ref, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map** | **Number**| The Map Id you are querying | 
 **key** | **String**| access key | 
 **ref** | **String**| ref id | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="locationsLocationIdGet"></a>
# **locationsLocationIdGet**
> locationsLocationIdGet(locationId, map, key)

locations summary

locations description

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.LocationsApi();

var locationId = 1.2; // Number | location id

var map = 1.2; // Number | The Map Id you are querying

var key = "key_example"; // String | The authorization Key required for use by the Map.


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.locationsLocationIdGet(locationId, map, key, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **locationId** | **Number**| location id | 
 **map** | **Number**| The Map Id you are querying | 
 **key** | **String**| The authorization Key required for use by the Map. | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

