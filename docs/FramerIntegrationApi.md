# FramerIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**framerCreateTemplate**](FramerIntegrationApi.md#framerCreateTemplate) | **POST** /v1/framer/templates | Create Framer Template |
| [**framerDeleteTemplate**](FramerIntegrationApi.md#framerDeleteTemplate) | **DELETE** /v1/framer/templates/{id} | Delete Framer Template |
| [**framerGetTemplate**](FramerIntegrationApi.md#framerGetTemplate) | **GET** /v1/framer/templates/{id} | Retrieve Framer Template |
| [**framerListTemplates**](FramerIntegrationApi.md#framerListTemplates) | **GET** /v1/framer/templates | List Framer Templates |
| [**framerUpdateTemplate**](FramerIntegrationApi.md#framerUpdateTemplate) | **PUT** /v1/framer/templates/{id} | Update Framer Template |


<a id="framerCreateTemplate"></a>
# **framerCreateTemplate**
> FramerTemplateResponseDto framerCreateTemplate(createFramerTemplateDto)

Create Framer Template

Registers a new Framer template with its public remix link for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.FramerIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    FramerIntegrationApi apiInstance = new FramerIntegrationApi(defaultClient);
    CreateFramerTemplateDto createFramerTemplateDto = new CreateFramerTemplateDto(); // CreateFramerTemplateDto | 
    try {
      FramerTemplateResponseDto result = apiInstance.framerCreateTemplate(createFramerTemplateDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FramerIntegrationApi#framerCreateTemplate");
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
| **createFramerTemplateDto** | [**CreateFramerTemplateDto**](CreateFramerTemplateDto.md)|  | |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Template created successfully. |  -  |

<a id="framerDeleteTemplate"></a>
# **framerDeleteTemplate**
> framerDeleteTemplate(id)

Delete Framer Template

Deletes a registered Framer template for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.FramerIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    FramerIntegrationApi apiInstance = new FramerIntegrationApi(defaultClient);
    String id = "id_example"; // String | The Framer template ID
    try {
      apiInstance.framerDeleteTemplate(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling FramerIntegrationApi#framerDeleteTemplate");
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
| **id** | **String**| The Framer template ID | |

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
| **204** | Template deleted successfully. |  -  |

<a id="framerGetTemplate"></a>
# **framerGetTemplate**
> FramerTemplateResponseDto framerGetTemplate(id)

Retrieve Framer Template

Retrieves details of a specific registered Framer template.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.FramerIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    FramerIntegrationApi apiInstance = new FramerIntegrationApi(defaultClient);
    String id = "id_example"; // String | The Framer template ID
    try {
      FramerTemplateResponseDto result = apiInstance.framerGetTemplate(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FramerIntegrationApi#framerGetTemplate");
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
| **id** | **String**| The Framer template ID | |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Details of the Framer template. |  -  |

<a id="framerListTemplates"></a>
# **framerListTemplates**
> List&lt;FramerTemplateResponseDto&gt; framerListTemplates()

List Framer Templates

Retrieves all registered Framer templates for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.FramerIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    FramerIntegrationApi apiInstance = new FramerIntegrationApi(defaultClient);
    try {
      List<FramerTemplateResponseDto> result = apiInstance.framerListTemplates();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FramerIntegrationApi#framerListTemplates");
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

[**List&lt;FramerTemplateResponseDto&gt;**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of Framer templates. |  -  |

<a id="framerUpdateTemplate"></a>
# **framerUpdateTemplate**
> FramerTemplateResponseDto framerUpdateTemplate(id, updateFramerTemplateDto)

Update Framer Template

Updates a registered Framer template for the active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.FramerIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    FramerIntegrationApi apiInstance = new FramerIntegrationApi(defaultClient);
    String id = "id_example"; // String | The Framer template ID
    UpdateFramerTemplateDto updateFramerTemplateDto = new UpdateFramerTemplateDto(); // UpdateFramerTemplateDto | 
    try {
      FramerTemplateResponseDto result = apiInstance.framerUpdateTemplate(id, updateFramerTemplateDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FramerIntegrationApi#framerUpdateTemplate");
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
| **id** | **String**| The Framer template ID | |
| **updateFramerTemplateDto** | [**UpdateFramerTemplateDto**](UpdateFramerTemplateDto.md)|  | |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template updated successfully. |  -  |

