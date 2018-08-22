# atlas_backend_api

AtlasBackendApi - JavaScript client for atlas_backend_api
Atlas Backend API documentation with Swagger
This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.JavascriptClientCodegen

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install atlas_backend_api --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your atlas_backend_api from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('atlas_backend_api')` in javascript files from the directory you ran the last 
command above from.

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/YOUR_USERNAME/atlas_backend_api
then install it via:

```shell
    npm install YOUR_USERNAME/atlas_backend_api --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var AtlasBackendApi = require('atlas_backend_api');

var api = new AtlasBackendApi.CategoriesApi()

var categoryId = 1.2; // {Number} This is the category Id that you are asking information about

var map = 1.2; // {Number} The Map Id you are querying

var key = "key_example"; // {String} THe authorization Key required for use by the Map.

var opts = { 
  'children': "children_example" // {String} Including this in your query will return the list of children categories and locations under the queried category.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.categoriesCategoryIdGet(categoryId, map, key, opts, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://dev.concept3d.com:8888*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AtlasBackendApi.CategoriesApi* | [**categoriesCategoryIdGet**](docs/CategoriesApi.md#categoriesCategoryIdGet) | **GET** /categories/{categoryId} | Categories summary
*AtlasBackendApi.CategoriesApi* | [**categoriesGet**](docs/CategoriesApi.md#categoriesGet) | **GET** /categories | endpoint dedicated to information about categories and their children locations.
*AtlasBackendApi.ConfigApi* | [**configGet**](docs/ConfigApi.md#configGet) | **GET** /config | endpoint to return map configuration information
*AtlasBackendApi.LocationsApi* | [**locationsGet**](docs/LocationsApi.md#locationsGet) | **GET** /locations | Locations Endpoint.  Does not use a location ID
*AtlasBackendApi.LocationsApi* | [**locationsLocationIdGet**](docs/LocationsApi.md#locationsLocationIdGet) | **GET** /locations/{locationId} | locations summary
*AtlasBackendApi.SearchApi* | [**searchGet**](docs/SearchApi.md#searchGet) | **GET** /search | search summary
*AtlasBackendApi.StylesApi* | [**stylesGet**](docs/StylesApi.md#stylesGet) | **GET** /styles | styles API returns CSS for Styles from CMS
*AtlasBackendApi.ToursApi* | [**toursGet**](docs/ToursApi.md#toursGet) | **GET** /tours | Tours API without a Tour ID
*AtlasBackendApi.ToursApi* | [**toursTourIdGet**](docs/ToursApi.md#toursTourIdGet) | **GET** /tours/{tourId} | 
*AtlasBackendApi.WayfindingApi* | [**wayfindingGet**](docs/WayfindingApi.md#wayfindingGet) | **GET** /wayfinding | search summary


## Documentation for Models

 - [AtlasBackendApi.Error](docs/Error.md)


## Documentation for Authorization

 All endpoints do not require authorization.

