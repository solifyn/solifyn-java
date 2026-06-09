# ProductsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**productsArchive**](ProductsApi.md#productsArchive) | **DELETE** /v1/products/{id} | Archive Product |
| [**productsCreate**](ProductsApi.md#productsCreate) | **POST** /v1/products | Create Product |
| [**productsGet**](ProductsApi.md#productsGet) | **GET** /v1/products/{id} | Retrieve Product |
| [**productsList**](ProductsApi.md#productsList) | **GET** /v1/products | List Products |
| [**productsUnarchive**](ProductsApi.md#productsUnarchive) | **POST** /v1/products/{id}/unarchive | Unarchive Product |
| [**productsUpdate**](ProductsApi.md#productsUpdate) | **PATCH** /v1/products/{id} | Update Product |


<a id="productsArchive"></a>
# **productsArchive**
> ProductsArchive200Response productsArchive(id)

Archive Product

Archive a specific product to hide it from checkout pages and search results. Products are soft-deleted (archived) and can be restored using the unarchive endpoint.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "prod_123"; // String | The unique product ID to archive.
    try {
      ProductsArchive200Response result = apiInstance.productsArchive(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#productsArchive");
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
| **id** | **String**| The unique product ID to archive. | |

### Return type

[**ProductsArchive200Response**](ProductsArchive200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product archived successfully. |  -  |

<a id="productsCreate"></a>
# **productsCreate**
> Product productsCreate(productCreate)

Create Product

Create a new product within your active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    ProductCreate productCreate = new ProductCreate(); // ProductCreate | 
    try {
      Product result = apiInstance.productsCreate(productCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#productsCreate");
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
| **productCreate** | [**ProductCreate**](ProductCreate.md)|  | |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product created successfully. |  -  |

<a id="productsGet"></a>
# **productsGet**
> Product productsGet(id)

Retrieve Product

Retrieve details of a specific product using its ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "prod_123"; // String | The unique product ID.
    try {
      Product result = apiInstance.productsGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#productsGet");
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
| **id** | **String**| The unique product ID. | |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved product details. |  -  |

<a id="productsList"></a>
# **productsList**
> ProductsList200Response productsList(pricingType, sorting, limit, page, isRecurring, isArchived, query, id)

List Products

List and query products belonging to your active business with support for fuzzy search, filters, pagination, and sorting.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String pricingType = "pricingType_example"; // String | Filter by pricing type.
    String sorting = "created_at"; // String | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order.
    BigDecimal limit = new BigDecimal("10"); // BigDecimal | Size of a page, defaults to 10. Maximum is 100.
    BigDecimal page = new BigDecimal("1"); // BigDecimal | Page number, defaults to 1.
    Boolean isRecurring = true; // Boolean | Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned.
    Boolean isArchived = true; // Boolean | Filter by archived status.
    String query = "query_example"; // String | Filter by product name (fuzzy, case-insensitive).
    String id = "id_example"; // String | Filter by product ID.
    try {
      ProductsList200Response result = apiInstance.productsList(pricingType, sorting, limit, page, isRecurring, isArchived, query, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#productsList");
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
| **pricingType** | **String**| Filter by pricing type. | [optional] |
| **sorting** | **String**| Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional] [enum: created_at, -created_at, name, -name, price_amount, -price_amount] |
| **limit** | **BigDecimal**| Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10] |
| **page** | **BigDecimal**| Page number, defaults to 1. | [optional] [default to 1] |
| **isRecurring** | **Boolean**| Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned. | [optional] |
| **isArchived** | **Boolean**| Filter by archived status. | [optional] |
| **query** | **String**| Filter by product name (fuzzy, case-insensitive). | [optional] |
| **id** | **String**| Filter by product ID. | [optional] |

### Return type

[**ProductsList200Response**](ProductsList200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved products list. |  -  |

<a id="productsUnarchive"></a>
# **productsUnarchive**
> ProductsUnarchive200Response productsUnarchive(id)

Unarchive Product

Restore an archived product back to active status, making it visible again.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "prod_123"; // String | The unique product ID to unarchive.
    try {
      ProductsUnarchive200Response result = apiInstance.productsUnarchive(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#productsUnarchive");
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
| **id** | **String**| The unique product ID to unarchive. | |

### Return type

[**ProductsUnarchive200Response**](ProductsUnarchive200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product unarchived successfully. |  -  |

<a id="productsUpdate"></a>
# **productsUpdate**
> ProductMessageResponseDto productsUpdate(id, productUpdate)

Update Product

Update details of an existing product.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.ProductsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    ProductsApi apiInstance = new ProductsApi(defaultClient);
    String id = "prod_123"; // String | The unique product ID.
    ProductUpdate productUpdate = new ProductUpdate(); // ProductUpdate | 
    try {
      ProductMessageResponseDto result = apiInstance.productsUpdate(id, productUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProductsApi#productsUpdate");
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
| **id** | **String**| The unique product ID. | |
| **productUpdate** | [**ProductUpdate**](ProductUpdate.md)|  | |

### Return type

[**ProductMessageResponseDto**](ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product updated successfully. |  -  |

