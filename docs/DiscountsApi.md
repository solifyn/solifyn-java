# DiscountsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**discountsCreate**](DiscountsApi.md#discountsCreate) | **POST** /v1/discounts | Create Discount |
| [**discountsDelete**](DiscountsApi.md#discountsDelete) | **DELETE** /v1/discounts/{id} | Delete Discount |
| [**discountsGet**](DiscountsApi.md#discountsGet) | **GET** /v1/discounts/{id} | Retrieve Discount |
| [**discountsList**](DiscountsApi.md#discountsList) | **GET** /v1/discounts | List Discounts |
| [**discountsUpdate**](DiscountsApi.md#discountsUpdate) | **PATCH** /v1/discounts/{id} | Update Discount |
| [**discountsValidate**](DiscountsApi.md#discountsValidate) | **GET** /v1/discounts/validate | Validate Code |


<a id="discountsCreate"></a>
# **discountsCreate**
> Discount discountsCreate(discountCreate)

Create Discount

Create a new discount code within your active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DiscountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DiscountsApi apiInstance = new DiscountsApi(defaultClient);
    DiscountCreate discountCreate = new DiscountCreate(); // DiscountCreate | 
    try {
      Discount result = apiInstance.discountsCreate(discountCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscountsApi#discountsCreate");
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
| **discountCreate** | [**DiscountCreate**](DiscountCreate.md)|  | |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Discount created successfully. |  -  |

<a id="discountsDelete"></a>
# **discountsDelete**
> LicensesDeactivate200Response discountsDelete(id)

Delete Discount

Delete a specific discount code by ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DiscountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DiscountsApi apiInstance = new DiscountsApi(defaultClient);
    String id = "disc_123"; // String | The unique discount ID.
    try {
      LicensesDeactivate200Response result = apiInstance.discountsDelete(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscountsApi#discountsDelete");
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
| **id** | **String**| The unique discount ID. | |

### Return type

[**LicensesDeactivate200Response**](LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount deleted successfully. |  -  |

<a id="discountsGet"></a>
# **discountsGet**
> Discount discountsGet(id)

Retrieve Discount

Retrieve details of a specific discount code using its ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DiscountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DiscountsApi apiInstance = new DiscountsApi(defaultClient);
    String id = "disc_123"; // String | The unique discount ID.
    try {
      Discount result = apiInstance.discountsGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscountsApi#discountsGet");
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
| **id** | **String**| The unique discount ID. | |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved discount details. |  -  |

<a id="discountsList"></a>
# **discountsList**
> DiscountsList200Response discountsList(sorting, limit, page, query, id)

List Discounts

List and query discounts belonging to your active business with support for fuzzy search by code, pagination, and sorting.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DiscountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DiscountsApi apiInstance = new DiscountsApi(defaultClient);
    String sorting = "created_at"; // String | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order.
    BigDecimal limit = new BigDecimal("10"); // BigDecimal | Size of a page, defaults to 10. Maximum is 100.
    BigDecimal page = new BigDecimal("1"); // BigDecimal | Page number, defaults to 1.
    String query = "query_example"; // String | Filter by discount code (fuzzy, case-insensitive).
    String id = "id_example"; // String | Filter by discount ID.
    try {
      DiscountsList200Response result = apiInstance.discountsList(sorting, limit, page, query, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscountsApi#discountsList");
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
| **sorting** | **String**| Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional] [enum: created_at, -created_at] |
| **limit** | **BigDecimal**| Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10] |
| **page** | **BigDecimal**| Page number, defaults to 1. | [optional] [default to 1] |
| **query** | **String**| Filter by discount code (fuzzy, case-insensitive). | [optional] |
| **id** | **String**| Filter by discount ID. | [optional] |

### Return type

[**DiscountsList200Response**](DiscountsList200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved discounts list. |  -  |

<a id="discountsUpdate"></a>
# **discountsUpdate**
> Discount discountsUpdate(id, discountUpdate)

Update Discount

Update details of an existing discount code.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DiscountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DiscountsApi apiInstance = new DiscountsApi(defaultClient);
    String id = "disc_123"; // String | The unique discount ID.
    DiscountUpdate discountUpdate = new DiscountUpdate(); // DiscountUpdate | 
    try {
      Discount result = apiInstance.discountsUpdate(id, discountUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscountsApi#discountsUpdate");
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
| **id** | **String**| The unique discount ID. | |
| **discountUpdate** | [**DiscountUpdate**](DiscountUpdate.md)|  | |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount updated successfully. |  -  |

<a id="discountsValidate"></a>
# **discountsValidate**
> Discount discountsValidate(code, businessId)

Validate Code

Validate if a specific discount code is active and valid for purchase checkout.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DiscountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DiscountsApi apiInstance = new DiscountsApi(defaultClient);
    String code = "SAVE20"; // String | The plain discount code string
    String businessId = "biz_123"; // String | The business database ID context
    try {
      Discount result = apiInstance.discountsValidate(code, businessId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscountsApi#discountsValidate");
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
| **code** | **String**| The plain discount code string | |
| **businessId** | **String**| The business database ID context | |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation query results. |  -  |

