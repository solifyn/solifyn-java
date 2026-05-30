# PayoutsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**payoutsCreateWithdrawal**](PayoutsApi.md#payoutsCreateWithdrawal) | **POST** /v1/payouts/withdrawals | Create Withdrawal |
| [**payoutsGetAccount**](PayoutsApi.md#payoutsGetAccount) | **GET** /v1/payouts/account | Retrieve Payout Account |
| [**payoutsGetAccountLink**](PayoutsApi.md#payoutsGetAccountLink) | **GET** /v1/payouts/account-link | Create Account Link |
| [**payoutsGetToken**](PayoutsApi.md#payoutsGetToken) | **GET** /v1/payouts/token | Generate Portal Access Token |
| [**payoutsGetWithdrawals**](PayoutsApi.md#payoutsGetWithdrawals) | **GET** /v1/payouts/withdrawals | Get Withdrawals List |
| [**payoutsListMethods**](PayoutsApi.md#payoutsListMethods) | **GET** /v1/payouts/methods | List Payout Methods |
| [**payoutsListVerifications**](PayoutsApi.md#payoutsListVerifications) | **GET** /v1/payouts/verifications | List Verifications |
| [**payoutsListWithdrawals**](PayoutsApi.md#payoutsListWithdrawals) | **GET** /v1/payouts | List Withdrawals |


<a id="payoutsCreateWithdrawal"></a>
# **payoutsCreateWithdrawal**
> Withdrawal payoutsCreateWithdrawal(withdrawalCreate)

Create Withdrawal

Initiate a balance withdrawal transfer request.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    WithdrawalCreate withdrawalCreate = new WithdrawalCreate(); // WithdrawalCreate | 
    try {
      Withdrawal result = apiInstance.payoutsCreateWithdrawal(withdrawalCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsCreateWithdrawal");
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
| **withdrawalCreate** | [**WithdrawalCreate**](WithdrawalCreate.md)|  | |

### Return type

[**Withdrawal**](Withdrawal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Withdrawal successfully initiated. |  -  |

<a id="payoutsGetAccount"></a>
# **payoutsGetAccount**
> PayoutAccount payoutsGetAccount()

Retrieve Payout Account

Retrieve general status and information of onboarding payout accounts.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    try {
      PayoutAccount result = apiInstance.payoutsGetAccount();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsGetAccount");
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

[**PayoutAccount**](PayoutAccount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payout account details retrieved successfully. |  -  |

<a id="payoutsGetAccountLink"></a>
# **payoutsGetAccountLink**
> PayoutAccountLink payoutsGetAccountLink(useCase)

Create Account Link

Generate temporary links for onboarding or viewing portals.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    String useCase = "account_onboarding"; // String | Onboarding link type context
    try {
      PayoutAccountLink result = apiInstance.payoutsGetAccountLink(useCase);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsGetAccountLink");
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
| **useCase** | **String**| Onboarding link type context | [optional] [enum: account_onboarding, payouts_portal] |

### Return type

[**PayoutAccountLink**](PayoutAccountLink.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account connection link generated. |  -  |

<a id="payoutsGetToken"></a>
# **payoutsGetToken**
> PayoutAccessToken payoutsGetToken()

Generate Portal Access Token

Generate temporary credentials to access the embed portal.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    try {
      PayoutAccessToken result = apiInstance.payoutsGetToken();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsGetToken");
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

[**PayoutAccessToken**](PayoutAccessToken.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Portal access token successfully generated. |  -  |

<a id="payoutsGetWithdrawals"></a>
# **payoutsGetWithdrawals**
> WithdrawalList payoutsGetWithdrawals(limit, page)

Get Withdrawals List

Retrieve withdrawal records for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Page size limit
    BigDecimal page = new BigDecimal(78); // BigDecimal | Page number
    try {
      WithdrawalList result = apiInstance.payoutsGetWithdrawals(limit, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsGetWithdrawals");
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
| **limit** | **BigDecimal**| Page size limit | [optional] |
| **page** | **BigDecimal**| Page number | [optional] |

### Return type

[**WithdrawalList**](WithdrawalList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Withdrawals list retrieved successfully. |  -  |

<a id="payoutsListMethods"></a>
# **payoutsListMethods**
> PayoutMethodList payoutsListMethods(limit, page)

List Payout Methods

List saved payout destinations (bank accounts, cards).

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    BigDecimal limit = new BigDecimal(78); // BigDecimal | 
    BigDecimal page = new BigDecimal(78); // BigDecimal | 
    try {
      PayoutMethodList result = apiInstance.payoutsListMethods(limit, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsListMethods");
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
| **limit** | **BigDecimal**|  | [optional] |
| **page** | **BigDecimal**|  | [optional] |

### Return type

[**PayoutMethodList**](PayoutMethodList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payout methods retrieved successfully. |  -  |

<a id="payoutsListVerifications"></a>
# **payoutsListVerifications**
> PayoutVerificationList payoutsListVerifications(limit, page)

List Verifications

Retrieve pending or completed KYC verification checks.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    BigDecimal limit = new BigDecimal(78); // BigDecimal | 
    BigDecimal page = new BigDecimal(78); // BigDecimal | 
    try {
      PayoutVerificationList result = apiInstance.payoutsListVerifications(limit, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsListVerifications");
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
| **limit** | **BigDecimal**|  | [optional] |
| **page** | **BigDecimal**|  | [optional] |

### Return type

[**PayoutVerificationList**](PayoutVerificationList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | KYC verifications list retrieved. |  -  |

<a id="payoutsListWithdrawals"></a>
# **payoutsListWithdrawals**
> WithdrawalList payoutsListWithdrawals(limit, page)

List Withdrawals

Retrieve a list of past withdrawal history.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.PayoutsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    PayoutsApi apiInstance = new PayoutsApi(defaultClient);
    BigDecimal limit = new BigDecimal(78); // BigDecimal | Page size limit
    BigDecimal page = new BigDecimal(78); // BigDecimal | Page number
    try {
      WithdrawalList result = apiInstance.payoutsListWithdrawals(limit, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PayoutsApi#payoutsListWithdrawals");
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
| **limit** | **BigDecimal**| Page size limit | [optional] |
| **page** | **BigDecimal**| Page number | [optional] |

### Return type

[**WithdrawalList**](WithdrawalList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Withdrawals list retrieved successfully. |  -  |

