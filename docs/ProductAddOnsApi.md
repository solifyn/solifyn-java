# ProductAddOnsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**productsCreateAddon**](ProductAddOnsApi.md#productsCreateAddon) | **POST** /v1/products/{id}/addons | Create Product Add-on |
| [**productsDeleteAddon**](ProductAddOnsApi.md#productsDeleteAddon) | **DELETE** /v1/products/{id}/addons/{addonId} | Delete Product Add-on |
| [**productsGetAddon**](ProductAddOnsApi.md#productsGetAddon) | **GET** /v1/products/{id}/addons/{addonId} | Retrieve Product Add-on |
| [**productsListAddons**](ProductAddOnsApi.md#productsListAddons) | **GET** /v1/products/{id}/addons | List Product Add-ons |
| [**productsListAllAddons**](ProductAddOnsApi.md#productsListAllAddons) | **GET** /v1/products/all-addons/list | List All Add-ons |
| [**productsUpdateAddon**](ProductAddOnsApi.md#productsUpdateAddon) | **PATCH** /v1/products/{id}/addons/{addonId} | Update Product Add-on |


<a id="productsCreateAddon"></a>
# **productsCreateAddon**
> Addon productsCreateAddon(id, addonCreate)

Create Product Add-on

Attach a new add-on configuration to a product.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductAddOnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductAddOnsApi apiInstance = new ProductAddOnsApi(defaultClient);
    String id = "prod_parent_123"; // String | The parent product ID.
    AddonCreate addonCreate = new AddonCreate(); // AddonCreate | 
    try {
      Addon result = apiInstance.productsCreateAddon(id, addonCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductAddOnsApi#productsCreateAddon");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| The parent product ID. | |
| **addonCreate** | [**AddonCreate**](AddonCreate.md)|  | |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Add-on attached successfully. |  -  |

<a id="productsDeleteAddon"></a>
# **productsDeleteAddon**
> ProductMessageResponseDto productsDeleteAddon(id, addonId)

Delete Product Add-on

Remove an add-on configuration from a product.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductAddOnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductAddOnsApi apiInstance = new ProductAddOnsApi(defaultClient);
    String id = "prod_parent_123"; // String | The parent product ID.
    String addonId = "prod_addon_123"; // String | The add-on product ID to remove.
    try {
      ProductMessageResponseDto result = apiInstance.productsDeleteAddon(id, addonId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductAddOnsApi#productsDeleteAddon");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| The parent product ID. | |
| **addonId** | **String**| The add-on product ID to remove. | |

### Return type

[**ProductMessageResponseDto**](ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Add-on configuration removed successfully. |  -  |

<a id="productsGetAddon"></a>
# **productsGetAddon**
> Addon productsGetAddon(id, addonId)

Retrieve Product Add-on

Retrieve a specific add-on configuration of a product.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductAddOnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductAddOnsApi apiInstance = new ProductAddOnsApi(defaultClient);
    String id = "prod_parent_123"; // String | The parent product ID.
    String addonId = "prod_addon_123"; // String | The add-on product ID.
    try {
      Addon result = apiInstance.productsGetAddon(id, addonId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductAddOnsApi#productsGetAddon");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| The parent product ID. | |
| **addonId** | **String**| The add-on product ID. | |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved add-on configuration. |  -  |

<a id="productsListAddons"></a>
# **productsListAddons**
> List&lt;Addon&gt; productsListAddons(id)

List Product Add-ons

Retrieve all add-on configurations attached to a product.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductAddOnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductAddOnsApi apiInstance = new ProductAddOnsApi(defaultClient);
    String id = "prod_parent_123"; // String | The parent product ID.
    try {
      List<Addon> result = apiInstance.productsListAddons(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductAddOnsApi#productsListAddons");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| The parent product ID. | |

### Return type

[**List&lt;Addon&gt;**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of product add-on configurations. |  -  |

<a id="productsListAllAddons"></a>
# **productsListAllAddons**
> productsListAllAddons()

List All Add-ons

Retrieve all configured add-on configurations for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductAddOnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductAddOnsApi apiInstance = new ProductAddOnsApi(defaultClient);
    try {
      apiInstance.productsListAllAddons();
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductAddOnsApi#productsListAllAddons");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved list of all addons. |  -  |

<a id="productsUpdateAddon"></a>
# **productsUpdateAddon**
> Addon productsUpdateAddon(id, addonId, addonUpdate)

Update Product Add-on

Update an existing add-on configuration for a product.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductAddOnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductAddOnsApi apiInstance = new ProductAddOnsApi(defaultClient);
    String id = "prod_parent_123"; // String | The parent product ID.
    String addonId = "prod_addon_123"; // String | The add-on product ID.
    AddonUpdate addonUpdate = new AddonUpdate(); // AddonUpdate | 
    try {
      Addon result = apiInstance.productsUpdateAddon(id, addonId, addonUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductAddOnsApi#productsUpdateAddon");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**| The parent product ID. | |
| **addonId** | **String**| The add-on product ID. | |
| **addonUpdate** | [**AddonUpdate**](AddonUpdate.md)|  | |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Add-on configuration updated successfully. |  -  |

