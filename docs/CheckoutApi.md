# CheckoutApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**checkoutCreate**](CheckoutApi.md#checkoutCreate) | **POST** /v1/checkout/create | Create Checkout Session |
| [**checkoutCreateCollection**](CheckoutApi.md#checkoutCreateCollection) | **POST** /v1/checkout/collection/create | Create Collection Checkout Session |
| [**checkoutCreateSetup**](CheckoutApi.md#checkoutCreateSetup) | **POST** /v1/checkout/setup-configuration | Create Setup Checkout Configuration |
| [**checkoutGetSession**](CheckoutApi.md#checkoutGetSession) | **GET** /v1/checkout/session/{id} | Get Checkout Session Details |
| [**checkoutPricePreview**](CheckoutApi.md#checkoutPricePreview) | **GET** /v1/checkout/price-preview | Get Converted Price Preview |
| [**checkoutSupportedCurrencies**](CheckoutApi.md#checkoutSupportedCurrencies) | **GET** /v1/checkout/supported-currencies | Get Supported Currencies |


<a id="checkoutCreate"></a>
# **checkoutCreate**
> CheckoutResponseDto checkoutCreate(createCheckoutDto)

Create Checkout Session

Create a new payment configuration for a product. Returns redirect URLs pointing to the custom checkout layout.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CheckoutApi apiInstance = new CheckoutApi(defaultClient);
    CreateCheckoutDto createCheckoutDto = new CreateCheckoutDto(); // CreateCheckoutDto | 
    try {
      CheckoutResponseDto result = apiInstance.checkoutCreate(createCheckoutDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutApi#checkoutCreate");
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
| **createCheckoutDto** | [**CreateCheckoutDto**](CreateCheckoutDto.md)|  | |

### Return type

[**CheckoutResponseDto**](CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Checkout session configuration created successfully. |  -  |

<a id="checkoutCreateCollection"></a>
# **checkoutCreateCollection**
> CheckoutResponseDto checkoutCreateCollection(createCollectionCheckoutDto)

Create Collection Checkout Session

Create a new payment configuration for a product bundle/collection.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CheckoutApi apiInstance = new CheckoutApi(defaultClient);
    CreateCollectionCheckoutDto createCollectionCheckoutDto = new CreateCollectionCheckoutDto(); // CreateCollectionCheckoutDto | 
    try {
      CheckoutResponseDto result = apiInstance.checkoutCreateCollection(createCollectionCheckoutDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutApi#checkoutCreateCollection");
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
| **createCollectionCheckoutDto** | [**CreateCollectionCheckoutDto**](CreateCollectionCheckoutDto.md)|  | |

### Return type

[**CheckoutResponseDto**](CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Collection checkout session created. |  -  |

<a id="checkoutCreateSetup"></a>
# **checkoutCreateSetup**
> checkoutCreateSetup(createSetupCheckoutDto)

Create Setup Checkout Configuration

Create a new checkout session in setup mode for collecting cards without immediate charge.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CheckoutApi apiInstance = new CheckoutApi(defaultClient);
    CreateSetupCheckoutDto createSetupCheckoutDto = new CreateSetupCheckoutDto(); // CreateSetupCheckoutDto | 
    try {
      apiInstance.checkoutCreateSetup(createSetupCheckoutDto);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutApi#checkoutCreateSetup");
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
| **createSetupCheckoutDto** | [**CreateSetupCheckoutDto**](CreateSetupCheckoutDto.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Setup checkout configuration created. |  -  |

<a id="checkoutGetSession"></a>
# **checkoutGetSession**
> CheckoutSessionDetailsDto checkoutGetSession(id)

Get Checkout Session Details

Retrieve checkout details to mount the custom embedded checkout.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CheckoutApi apiInstance = new CheckoutApi(defaultClient);
    String id = "ch_XXXXXXXXXXX"; // String | Internal database checkout session ID
    try {
      CheckoutSessionDetailsDto result = apiInstance.checkoutGetSession(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutApi#checkoutGetSession");
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
| **id** | **String**| Internal database checkout session ID | |

### Return type

[**CheckoutSessionDetailsDto**](CheckoutSessionDetailsDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout session details resolved. |  -  |

<a id="checkoutPricePreview"></a>
# **checkoutPricePreview**
> PricePreviewResponseDto checkoutPricePreview(productId, addons, currency, discount, qty, customPrice)

Get Converted Price Preview

Pre-calculate target currencies, applied discounts, and PWYW values before mounting the checkout.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CheckoutApi apiInstance = new CheckoutApi(defaultClient);
    String productId = "prod_z2o92kEl6cYYX"; // String | Public product ID
    String addons = "addons_example"; // String | 
    String currency = "vnd"; // String | Target currency code (ISO)
    String discount = "10"; // String | Percentage discount rate
    String qty = "1"; // String | Number of product units
    String customPrice = "15"; // String | Override price for PWYW products
    try {
      PricePreviewResponseDto result = apiInstance.checkoutPricePreview(productId, addons, currency, discount, qty, customPrice);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutApi#checkoutPricePreview");
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
| **productId** | **String**| Public product ID | |
| **addons** | **String**|  | |
| **currency** | **String**| Target currency code (ISO) | [optional] |
| **discount** | **String**| Percentage discount rate | [optional] |
| **qty** | **String**| Number of product units | [optional] |
| **customPrice** | **String**| Override price for PWYW products | [optional] |

### Return type

[**PricePreviewResponseDto**](PricePreviewResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Price preview calculations returned. |  -  |

<a id="checkoutSupportedCurrencies"></a>
# **checkoutSupportedCurrencies**
> List&lt;SupportedCurrenciesResponseDto&gt; checkoutSupportedCurrencies()

Get Supported Currencies

Retrieve all currencies supported for payouts and conversions.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CheckoutApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CheckoutApi apiInstance = new CheckoutApi(defaultClient);
    try {
      List<SupportedCurrenciesResponseDto> result = apiInstance.checkoutSupportedCurrencies();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutApi#checkoutSupportedCurrencies");
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

[**List&lt;SupportedCurrenciesResponseDto&gt;**](SupportedCurrenciesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Supported currencies resolved successfully. |  -  |

