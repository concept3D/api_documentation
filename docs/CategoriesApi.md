# AtlasBackendApi.CategoriesApi

All URIs are relative to *https://dev.concept3d.com:8888*

Method | HTTP request | Description
------------- | ------------- | -------------
[**categoriesCategoryIdGet**](CategoriesApi.md#categoriesCategoryIdGet) | **GET** /categories/{categoryId} | Categories summary
[**categoriesGet**](CategoriesApi.md#categoriesGet) | **GET** /categories | endpoint dedicated to information about categories and their children locations.


<a name="categoriesCategoryIdGet"></a>
# **categoriesCategoryIdGet**
> categoriesCategoryIdGet(categoryId, map, key, opts)

Categories summary

Categories endpoint description 

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.CategoriesApi();

var categoryId = 1.2; // Number | This is the category Id that you are asking information about

var map = 1.2; // Number | The Map Id you are querying

var key = "key_example"; // String | THe authorization Key required for use by the Map.

var opts = { 
  'children': "children_example" // String | Including this in your query will return the list of children categories and locations under the queried category.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.categoriesCategoryIdGet(categoryId, map, key, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categoryId** | **Number**| This is the category Id that you are asking information about | 
 **map** | **Number**| The Map Id you are querying | 
 **key** | **String**| THe authorization Key required for use by the Map. | 
 **children** | **String**| Including this in your query will return the list of children categories and locations under the queried category. | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="categoriesGet"></a>
# **categoriesGet**
> categoriesGet(map, key, opts)

endpoint dedicated to information about categories and their children locations.

It is important to note that the order is important. Parameters are processed in the following order: defaults,full,parent,childIds,children,parentIds. This means that if defaults is present, it does not matter what values precedes it.

### Example
```javascript
var AtlasBackendApi = require('atlas_backend_api');

var apiInstance = new AtlasBackendApi.CategoriesApi();

var map = 1.2; // Number | this is the map id you are requesting access for

var key = "key_example"; // String | This is a client specific key granting access to the data for the MAP ID above

var opts = { 
  'defaults': "defaults_example", // String | You can add defaults to the querysting simply as &defaults.  you do not need to add a specific value, but you can if you'd like, or your code generates it.  If you add this in your query, no other value matters, and the default categories will always be returned.
  'parent': 56, // Number | If parent = 0 is present, the list of parent categories (the categories found at the root of the sidebar) are returned.  This can be combined with the FULL parameter for more information
  'childIds': "childIds_example", // String | the existance of childIds will return an array of Category Id's that detail the Parent Child relationship.  The FULL keyword has no affect on this.  parent and default will override it.
  'parentIds': "parentIds_example", // String | the existance of parentIds will return an array of Category Id's that detail the Parent Child relationship.  The FULL keyword has no affect on this.  parent, default and childIds will override it.
  'full': "full_example" // String | Adding full to the query string will return all information regarding the category.  If you do not add full to the query string, you will return enough information to view the category in the sidebar. The default is to not include this.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.categoriesGet(map, key, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **map** | **Number**| this is the map id you are requesting access for | 
 **key** | **String**| This is a client specific key granting access to the data for the MAP ID above | 
 **defaults** | **String**| You can add defaults to the querysting simply as &amp;defaults.  you do not need to add a specific value, but you can if you&#39;d like, or your code generates it.  If you add this in your query, no other value matters, and the default categories will always be returned. | [optional] 
 **parent** | **Number**| If parent &#x3D; 0 is present, the list of parent categories (the categories found at the root of the sidebar) are returned.  This can be combined with the FULL parameter for more information | [optional] 
 **childIds** | **String**| the existance of childIds will return an array of Category Id&#39;s that detail the Parent Child relationship.  The FULL keyword has no affect on this.  parent and default will override it. | [optional] 
 **parentIds** | **String**| the existance of parentIds will return an array of Category Id&#39;s that detail the Parent Child relationship.  The FULL keyword has no affect on this.  parent, default and childIds will override it. | [optional] 
 **full** | **String**| Adding full to the query string will return all information regarding the category.  If you do not add full to the query string, you will return enough information to view the category in the sidebar. The default is to not include this. | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

