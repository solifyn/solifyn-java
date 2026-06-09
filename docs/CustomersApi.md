# CustomersApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**customersCreate**](CustomersApi.md#customersCreate) | **POST** /v1/customers | Create Customer |
| [**customersGenerateInvite**](CustomersApi.md#customersGenerateInvite) | **POST** /v1/customers/{id}/share | Generate Shared Invite |
| [**customersGet**](CustomersApi.md#customersGet) | **GET** /v1/customers/{id} | Retrieve Customer |
| [**customersList**](CustomersApi.md#customersList) | **GET** /v1/customers | List Customers |
| [**customersUpdate**](CustomersApi.md#customersUpdate) | **PATCH** /v1/customers/{id} | Update Customer |


<a id="customersCreate"></a>
# **customersCreate**
> CustomerResponseDto customersCreate(createCustomerDto)

Create Customer

Add/upsert a new customer profile under the current business context.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    CreateCustomerDto createCustomerDto = new CreateCustomerDto(); // CreateCustomerDto | 
    try {
      CustomerResponseDto result = apiInstance.customersCreate(createCustomerDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#customersCreate");
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
| **createCustomerDto** | [**CreateCustomerDto**](CreateCustomerDto.md)|  | |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Customer created/updated successfully. |  -  |

<a id="customersGenerateInvite"></a>
# **customersGenerateInvite**
> CustomerSharedInviteResponseDto customersGenerateInvite(id)

Generate Shared Invite

Generate a short-lived token granting temporary customer self-service billing page access.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "user_123"; // String | Customer ID
    try {
      CustomerSharedInviteResponseDto result = apiInstance.customersGenerateInvite(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#customersGenerateInvite");
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
| **id** | **String**| Customer ID | |

### Return type

[**CustomerSharedInviteResponseDto**](CustomerSharedInviteResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Self-service billing portal invite token created. |  -  |

<a id="customersGet"></a>
# **customersGet**
> CustomerResponseDto customersGet(id)

Retrieve Customer

Retrieve details of a customer profile by ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "user_123"; // String | Customer ID
    try {
      CustomerResponseDto result = apiInstance.customersGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#customersGet");
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
| **id** | **String**| Customer ID | |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Customer details retrieved successfully. |  -  |

<a id="customersList"></a>
# **customersList**
> CustomerListResponseDto customersList()

List Customers

Retrieve all customers associated with the current active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    try {
      CustomerListResponseDto result = apiInstance.customersList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#customersList");
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

[**CustomerListResponseDto**](CustomerListResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of customers retrieved successfully. |  -  |

<a id="customersUpdate"></a>
# **customersUpdate**
> CustomerMessageResponseDto customersUpdate(id, updateCustomerDto)

Update Customer

Update name, phone, or metadata of an existing customer profile.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.CustomersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    CustomersApi apiInstance = new CustomersApi(defaultClient);
    String id = "user_123"; // String | Customer ID
    UpdateCustomerDto updateCustomerDto = new UpdateCustomerDto(); // UpdateCustomerDto | 
    try {
      CustomerMessageResponseDto result = apiInstance.customersUpdate(id, updateCustomerDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomersApi#customersUpdate");
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
| **id** | **String**| Customer ID | |
| **updateCustomerDto** | [**UpdateCustomerDto**](UpdateCustomerDto.md)|  | |

### Return type

[**CustomerMessageResponseDto**](CustomerMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Customer updated successfully. |  -  |

