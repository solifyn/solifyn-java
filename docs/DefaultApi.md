# DefaultApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**disputeCreatedPost**](DefaultApi.md#disputeCreatedPost) | **POST** /dispute.created | Dispute Created |
| [**disputeLostPost**](DefaultApi.md#disputeLostPost) | **POST** /dispute.lost | Dispute Lost |
| [**disputeWonPost**](DefaultApi.md#disputeWonPost) | **POST** /dispute.won | Dispute Won |
| [**entitlementGrantCreatedPost**](DefaultApi.md#entitlementGrantCreatedPost) | **POST** /entitlement_grant.created | Entitlement Grant Created |
| [**entitlementGrantDeliveredPost**](DefaultApi.md#entitlementGrantDeliveredPost) | **POST** /entitlement_grant.delivered | Entitlement Grant Delivered |
| [**entitlementGrantFailedPost**](DefaultApi.md#entitlementGrantFailedPost) | **POST** /entitlement_grant.failed | Entitlement Grant Failed |
| [**entitlementGrantRevokedPost**](DefaultApi.md#entitlementGrantRevokedPost) | **POST** /entitlement_grant.revoked | Entitlement Grant Revoked |
| [**licenseCreatedPost**](DefaultApi.md#licenseCreatedPost) | **POST** /license.created | License Created |
| [**licenseRevokedPost**](DefaultApi.md#licenseRevokedPost) | **POST** /license.revoked | License Revoked |
| [**paymentCreatedPost**](DefaultApi.md#paymentCreatedPost) | **POST** /payment.created | Payment Created |
| [**paymentFailedPost**](DefaultApi.md#paymentFailedPost) | **POST** /payment.failed | Payment Failed |
| [**paymentSucceededPost**](DefaultApi.md#paymentSucceededPost) | **POST** /payment.succeeded | Payment Succeeded |
| [**refundFailedPost**](DefaultApi.md#refundFailedPost) | **POST** /refund.failed | Refund Failed |
| [**refundSucceededPost**](DefaultApi.md#refundSucceededPost) | **POST** /refund.succeeded | Refund Succeeded |
| [**subscriptionCreatedPost**](DefaultApi.md#subscriptionCreatedPost) | **POST** /subscription.created | Subscription Created |
| [**subscriptionDeactivatedPost**](DefaultApi.md#subscriptionDeactivatedPost) | **POST** /subscription.deactivated | Subscription Deactivated |
| [**subscriptionUpdatedPost**](DefaultApi.md#subscriptionUpdatedPost) | **POST** /subscription.updated | Subscription Updated |


<a id="disputeCreatedPost"></a>
# **disputeCreatedPost**
> disputeCreatedPost(webhookDisputePayload)

Dispute Created

Occurs when a payment charge is disputed by the customer (chargeback initiated).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookDisputePayload webhookDisputePayload = new WebhookDisputePayload(); // WebhookDisputePayload | 
    try {
      apiInstance.disputeCreatedPost(webhookDisputePayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#disputeCreatedPost");
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
| **webhookDisputePayload** | [**WebhookDisputePayload**](WebhookDisputePayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="disputeLostPost"></a>
# **disputeLostPost**
> disputeLostPost(webhookDisputePayload)

Dispute Lost

Occurs when a dispute challenge is lost and the funds are returned to the cardholder.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookDisputePayload webhookDisputePayload = new WebhookDisputePayload(); // WebhookDisputePayload | 
    try {
      apiInstance.disputeLostPost(webhookDisputePayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#disputeLostPost");
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
| **webhookDisputePayload** | [**WebhookDisputePayload**](WebhookDisputePayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="disputeWonPost"></a>
# **disputeWonPost**
> disputeWonPost(webhookDisputePayload)

Dispute Won

Occurs when a dispute challenge is won by the merchant.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookDisputePayload webhookDisputePayload = new WebhookDisputePayload(); // WebhookDisputePayload | 
    try {
      apiInstance.disputeWonPost(webhookDisputePayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#disputeWonPost");
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
| **webhookDisputePayload** | [**WebhookDisputePayload**](WebhookDisputePayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="entitlementGrantCreatedPost"></a>
# **entitlementGrantCreatedPost**
> entitlementGrantCreatedPost(webhookEntitlementGrantPayload)

Entitlement Grant Created

Occurs when a new entitlement grant is created (e.g., at checkout completion if the product has GitHub access). The collaborator invitation is pending.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookEntitlementGrantPayload webhookEntitlementGrantPayload = new WebhookEntitlementGrantPayload(); // WebhookEntitlementGrantPayload | 
    try {
      apiInstance.entitlementGrantCreatedPost(webhookEntitlementGrantPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#entitlementGrantCreatedPost");
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
| **webhookEntitlementGrantPayload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="entitlementGrantDeliveredPost"></a>
# **entitlementGrantDeliveredPost**
> entitlementGrantDeliveredPost(webhookEntitlementGrantPayload)

Entitlement Grant Delivered

Occurs when the customer successfully connects their GitHub account and the collaborator invitation is successfully delivered.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookEntitlementGrantPayload webhookEntitlementGrantPayload = new WebhookEntitlementGrantPayload(); // WebhookEntitlementGrantPayload | 
    try {
      apiInstance.entitlementGrantDeliveredPost(webhookEntitlementGrantPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#entitlementGrantDeliveredPost");
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
| **webhookEntitlementGrantPayload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="entitlementGrantFailedPost"></a>
# **entitlementGrantFailedPost**
> entitlementGrantFailedPost(webhookEntitlementGrantPayload)

Entitlement Grant Failed

Occurs when invitation delivery fails (e.g., if the user GitHub account is flagged or invitation limit is reached).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookEntitlementGrantPayload webhookEntitlementGrantPayload = new WebhookEntitlementGrantPayload(); // WebhookEntitlementGrantPayload | 
    try {
      apiInstance.entitlementGrantFailedPost(webhookEntitlementGrantPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#entitlementGrantFailedPost");
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
| **webhookEntitlementGrantPayload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="entitlementGrantRevokedPost"></a>
# **entitlementGrantRevokedPost**
> entitlementGrantRevokedPost(webhookEntitlementGrantPayload)

Entitlement Grant Revoked

Occurs when the customer access is removed from the repository (manually or automatically via subscription cancel/refund).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookEntitlementGrantPayload webhookEntitlementGrantPayload = new WebhookEntitlementGrantPayload(); // WebhookEntitlementGrantPayload | 
    try {
      apiInstance.entitlementGrantRevokedPost(webhookEntitlementGrantPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#entitlementGrantRevokedPost");
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
| **webhookEntitlementGrantPayload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="licenseCreatedPost"></a>
# **licenseCreatedPost**
> licenseCreatedPost(webhookLicensePayload)

License Created

Occurs when a new software license key is created or assigned to a customer purchase.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookLicensePayload webhookLicensePayload = new WebhookLicensePayload(); // WebhookLicensePayload | 
    try {
      apiInstance.licenseCreatedPost(webhookLicensePayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#licenseCreatedPost");
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
| **webhookLicensePayload** | [**WebhookLicensePayload**](WebhookLicensePayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="licenseRevokedPost"></a>
# **licenseRevokedPost**
> licenseRevokedPost(webhookLicensePayload)

License Revoked

Occurs when a software license key is revoked (e.g., due to subscription cancellation, refund, or dispute).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookLicensePayload webhookLicensePayload = new WebhookLicensePayload(); // WebhookLicensePayload | 
    try {
      apiInstance.licenseRevokedPost(webhookLicensePayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#licenseRevokedPost");
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
| **webhookLicensePayload** | [**WebhookLicensePayload**](WebhookLicensePayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="paymentCreatedPost"></a>
# **paymentCreatedPost**
> paymentCreatedPost(webhookPaymentPayload)

Payment Created

Occurs when a new payment is initiated (e.g., at checkout start or subscription creation). The payment may still be in an incomplete or pending state.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookPaymentPayload webhookPaymentPayload = new WebhookPaymentPayload(); // WebhookPaymentPayload | 
    try {
      apiInstance.paymentCreatedPost(webhookPaymentPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#paymentCreatedPost");
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
| **webhookPaymentPayload** | [**WebhookPaymentPayload**](WebhookPaymentPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="paymentFailedPost"></a>
# **paymentFailedPost**
> paymentFailedPost(order)

Payment Failed

Occurs when a customer payment attempt fails.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    Order order = new Order(); // Order | 
    try {
      apiInstance.paymentFailedPost(order);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#paymentFailedPost");
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
| **order** | [**Order**](Order.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="paymentSucceededPost"></a>
# **paymentSucceededPost**
> paymentSucceededPost(order)

Payment Succeeded

Occurs when a customer payment is confirmed as succeeded.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    Order order = new Order(); // Order | 
    try {
      apiInstance.paymentSucceededPost(order);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#paymentSucceededPost");
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
| **order** | [**Order**](Order.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="refundFailedPost"></a>
# **refundFailedPost**
> refundFailedPost(webhookRefundPayload)

Refund Failed

Occurs when a payment refund fails.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookRefundPayload webhookRefundPayload = new WebhookRefundPayload(); // WebhookRefundPayload | 
    try {
      apiInstance.refundFailedPost(webhookRefundPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#refundFailedPost");
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
| **webhookRefundPayload** | [**WebhookRefundPayload**](WebhookRefundPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="refundSucceededPost"></a>
# **refundSucceededPost**
> refundSucceededPost(webhookRefundPayload)

Refund Succeeded

Occurs when a payment refund is confirmed as succeeded.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookRefundPayload webhookRefundPayload = new WebhookRefundPayload(); // WebhookRefundPayload | 
    try {
      apiInstance.refundSucceededPost(webhookRefundPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#refundSucceededPost");
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
| **webhookRefundPayload** | [**WebhookRefundPayload**](WebhookRefundPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="subscriptionCreatedPost"></a>
# **subscriptionCreatedPost**
> subscriptionCreatedPost(webhookSubscriptionPayload)

Subscription Created

Occurs when a customer subscription is successfully started.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookSubscriptionPayload webhookSubscriptionPayload = new WebhookSubscriptionPayload(); // WebhookSubscriptionPayload | 
    try {
      apiInstance.subscriptionCreatedPost(webhookSubscriptionPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#subscriptionCreatedPost");
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
| **webhookSubscriptionPayload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="subscriptionDeactivatedPost"></a>
# **subscriptionDeactivatedPost**
> subscriptionDeactivatedPost(webhookSubscriptionPayload)

Subscription Deactivated

Occurs when a customer subscription is deactivated or expired.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookSubscriptionPayload webhookSubscriptionPayload = new WebhookSubscriptionPayload(); // WebhookSubscriptionPayload | 
    try {
      apiInstance.subscriptionDeactivatedPost(webhookSubscriptionPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#subscriptionDeactivatedPost");
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
| **webhookSubscriptionPayload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

<a id="subscriptionUpdatedPost"></a>
# **subscriptionUpdatedPost**
> subscriptionUpdatedPost(webhookSubscriptionPayload)

Subscription Updated

Occurs when a customer subscription is updated (e.g., cancel at period end changes).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    WebhookSubscriptionPayload webhookSubscriptionPayload = new WebhookSubscriptionPayload(); // WebhookSubscriptionPayload | 
    try {
      apiInstance.subscriptionUpdatedPost(webhookSubscriptionPayload);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#subscriptionUpdatedPost");
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
| **webhookSubscriptionPayload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully. |  -  |

