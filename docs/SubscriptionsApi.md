# SubscriptionsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**subscriptionsAction**](SubscriptionsApi.md#subscriptionsAction) | **POST** /v1/subscriptions/{subscriptionId}/{action} | Subscription Action |
| [**subscriptionsGet**](SubscriptionsApi.md#subscriptionsGet) | **GET** /v1/subscriptions/{id} | Retrieve Subscription Details |
| [**subscriptionsList**](SubscriptionsApi.md#subscriptionsList) | **GET** /v1/subscriptions | List Subscriptions |


<a id="subscriptionsAction"></a>
# **subscriptionsAction**
> SubscriptionsAction201Response subscriptionsAction(subscriptionId, action, subscriptionAction)

Subscription Action

Cancel, pause, resume, or add free days to a customer subscription.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    String subscriptionId = "mem_123"; // String | The customer subscription ID
    String action = "add_free_days"; // String | The subscription task to execute
    SubscriptionAction subscriptionAction = new SubscriptionAction(); // SubscriptionAction | 
    try {
      SubscriptionsAction201Response result = apiInstance.subscriptionsAction(subscriptionId, action, subscriptionAction);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#subscriptionsAction");
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
| **subscriptionId** | **String**| The customer subscription ID | |
| **action** | **String**| The subscription task to execute | [enum: add_free_days, cancel, pause, resume, uncancel, adjust_seats] |
| **subscriptionAction** | [**SubscriptionAction**](SubscriptionAction.md)|  | |

### Return type

[**SubscriptionsAction201Response**](SubscriptionsAction201Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Subscription action processed successfully. |  -  |

<a id="subscriptionsGet"></a>
# **subscriptionsGet**
> SubscriptionDetail subscriptionsGet(id)

Retrieve Subscription Details

Retrieve detailed information about a subscription and its billing history.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    String id = "mem_123"; // String | The customer subscription ID
    try {
      SubscriptionDetail result = apiInstance.subscriptionsGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#subscriptionsGet");
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
| **id** | **String**| The customer subscription ID | |

### Return type

[**SubscriptionDetail**](SubscriptionDetail.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Subscription details retrieved successfully. |  -  |

<a id="subscriptionsList"></a>
# **subscriptionsList**
> SubscriptionList subscriptionsList(customerId)

List Subscriptions

Retrieve a list of customer subscriptions, optionally filtered by customer ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.SubscriptionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    SubscriptionsApi apiInstance = new SubscriptionsApi(defaultClient);
    String customerId = "customerId_example"; // String | Filter subscriptions by customer ID.
    try {
      SubscriptionList result = apiInstance.subscriptionsList(customerId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionsApi#subscriptionsList");
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
| **customerId** | **String**| Filter subscriptions by customer ID. | [optional] |

### Return type

[**SubscriptionList**](SubscriptionList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Subscriptions retrieved successfully. |  -  |

