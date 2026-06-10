# CheckoutLinksApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**checkoutLinksCreate**](CheckoutLinksApi.md#checkoutLinksCreate) | **POST** /v1/checkout-links | Create Checkout Link |
| [**checkoutLinksDelete**](CheckoutLinksApi.md#checkoutLinksDelete) | **DELETE** /v1/checkout-links/{id} | Delete Checkout Link |
| [**checkoutLinksGet**](CheckoutLinksApi.md#checkoutLinksGet) | **GET** /v1/checkout-links/{id} | Retrieve Checkout Link Details |
| [**checkoutLinksList**](CheckoutLinksApi.md#checkoutLinksList) | **GET** /v1/checkout-links | List Checkout Links |
| [**checkoutLinksUpdate**](CheckoutLinksApi.md#checkoutLinksUpdate) | **PATCH** /v1/checkout-links/{id} | Update Checkout Link |


<a id="checkoutLinksCreate"></a>
# **checkoutLinksCreate**
> CheckoutLinkResponseDto checkoutLinksCreate(createCheckoutLinkDto)

Create Checkout Link

Generate a new checkout session link.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CheckoutLinksApi apiInstance = new CheckoutLinksApi(defaultClient);
    CreateCheckoutLinkDto createCheckoutLinkDto = new CreateCheckoutLinkDto(); // CreateCheckoutLinkDto | 
    try {
      CheckoutLinkResponseDto result = apiInstance.checkoutLinksCreate(createCheckoutLinkDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutLinksApi#checkoutLinksCreate");
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
| **createCheckoutLinkDto** | [**CreateCheckoutLinkDto**](CreateCheckoutLinkDto.md)|  | |

### Return type

[**CheckoutLinkResponseDto**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Checkout link created successfully. |  -  |

<a id="checkoutLinksDelete"></a>
# **checkoutLinksDelete**
> CheckoutLinkMessageResponseDto checkoutLinksDelete(id)

Delete Checkout Link

Permanently remove a checkout link.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CheckoutLinksApi apiInstance = new CheckoutLinksApi(defaultClient);
    String id = "chk_123"; // String | Checkout Link ID
    try {
      CheckoutLinkMessageResponseDto result = apiInstance.checkoutLinksDelete(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutLinksApi#checkoutLinksDelete");
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
| **id** | **String**| Checkout Link ID | |

### Return type

[**CheckoutLinkMessageResponseDto**](CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout link deleted successfully. |  -  |

<a id="checkoutLinksGet"></a>
# **checkoutLinksGet**
> CheckoutLinkResponseDto checkoutLinksGet(id)

Retrieve Checkout Link Details

Get details of a specific checkout link by ID (public access).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CheckoutLinksApi apiInstance = new CheckoutLinksApi(defaultClient);
    String id = "chk_123"; // String | Checkout Link ID
    try {
      CheckoutLinkResponseDto result = apiInstance.checkoutLinksGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutLinksApi#checkoutLinksGet");
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
| **id** | **String**| Checkout Link ID | |

### Return type

[**CheckoutLinkResponseDto**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout link resolved successfully. |  -  |

<a id="checkoutLinksList"></a>
# **checkoutLinksList**
> List&lt;CheckoutLinkResponseDto&gt; checkoutLinksList()

List Checkout Links

Retrieve all active checkout session links for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CheckoutLinksApi apiInstance = new CheckoutLinksApi(defaultClient);
    try {
      List<CheckoutLinkResponseDto> result = apiInstance.checkoutLinksList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutLinksApi#checkoutLinksList");
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

[**List&lt;CheckoutLinkResponseDto&gt;**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout links retrieved successfully. |  -  |

<a id="checkoutLinksUpdate"></a>
# **checkoutLinksUpdate**
> CheckoutLinkMessageResponseDto checkoutLinksUpdate(id, updateCheckoutLinkDto)

Update Checkout Link

Update title, custom pricing, redirection URLs, or friendly inputs for a checkout link.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutLinksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CheckoutLinksApi apiInstance = new CheckoutLinksApi(defaultClient);
    String id = "chk_123"; // String | Checkout Link ID
    UpdateCheckoutLinkDto updateCheckoutLinkDto = new UpdateCheckoutLinkDto(); // UpdateCheckoutLinkDto | 
    try {
      CheckoutLinkMessageResponseDto result = apiInstance.checkoutLinksUpdate(id, updateCheckoutLinkDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutLinksApi#checkoutLinksUpdate");
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
| **id** | **String**| Checkout Link ID | |
| **updateCheckoutLinkDto** | [**UpdateCheckoutLinkDto**](UpdateCheckoutLinkDto.md)|  | |

### Return type

[**CheckoutLinkMessageResponseDto**](CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout link updated successfully. |  -  |

