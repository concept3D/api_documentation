# AtlasBackendApi.ToursApi

All URIs are relative to *https://dev.concept3d.com:8888*

Method | HTTP request | Description
------------- | ------------- | -------------
[**toursGet**](ToursApi.md#toursGet) | **GET** /tours | Tours API without a Tour ID
[**toursTourIdGet**](ToursApi.md#toursTourIdGet) | **GET** /tours/{tourId} | 


<a name="toursGet"></a>
# **toursGet**
> toursGet(map, key, opts)

Tours API without a Tour ID

This Tour API works without a Tour ID.

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.ToursApi();

var map = 1.2; // Number | mapId

var key = "key_example"; // String | access key

var opts = { 
  'hierarchy': true, // Boolean | if used, this overrides all other variables.  This returns a structure of data that represents the groups andtours.  Only needed if group feature is used.
  'full': true // Boolean | This returns the full structure of data for all tours.  Not mobile friendly.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.toursGet(map, key, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map** | **Number**| mapId | 
 **key** | **String**| access key | 
 **hierarchy** | **Boolean**| if used, this overrides all other variables.  This returns a structure of data that represents the groups andtours.  Only needed if group feature is used. | [optional] 
 **full** | **Boolean**| This returns the full structure of data for all tours.  Not mobile friendly. | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="toursTourIdGet"></a>
# **toursTourIdGet**
> toursTourIdGet(tourId, map, key)



APi to return a specific Tour By ID

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.ToursApi();

var tourId = 1.2; // Number | location id

var map = 1.2; // Number | mapId

var key = "key_example"; // String | access key


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.toursTourIdGet(tourId, map, key, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tourId** | **Number**| location id | 
 **map** | **Number**| mapId | 
 **key** | **String**| access key | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

