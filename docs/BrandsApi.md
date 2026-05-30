# BrandsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**brandsCreate**](BrandsApi.md#brandsCreate) | **POST** /v1/user/brand | Create Brand |
| [**brandsGet**](BrandsApi.md#brandsGet) | **GET** /v1/user/brand/{id} | Retrieve Brand |
| [**brandsList**](BrandsApi.md#brandsList) | **GET** /v1/user/brands | List Brands |
| [**brandsUpdate**](BrandsApi.md#brandsUpdate) | **PATCH** /v1/user/brand/{id} | Update Brand |


<a id="brandsCreate"></a>
# **brandsCreate**
> Brand brandsCreate(brandCreate)

Create Brand

Add a new brand identity under the current active business.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BrandsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BrandsApi apiInstance = new BrandsApi(defaultClient);
    BrandCreate brandCreate = new BrandCreate(); // BrandCreate | 
    try {
      Brand result = apiInstance.brandsCreate(brandCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandsApi#brandsCreate");
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
| **brandCreate** | [**BrandCreate**](BrandCreate.md)|  | |

### Return type

[**Brand**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Brand successfully created. |  -  |

<a id="brandsGet"></a>
# **brandsGet**
> Brand brandsGet(id)

Retrieve Brand

Retrieve details of a brand identity by ID.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BrandsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BrandsApi apiInstance = new BrandsApi(defaultClient);
    String id = "brd_123"; // String | The brand ID to retrieve
    try {
      Brand result = apiInstance.brandsGet(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandsApi#brandsGet");
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
| **id** | **String**| The brand ID to retrieve | |

### Return type

[**Brand**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Brand details retrieved successfully. |  -  |

<a id="brandsList"></a>
# **brandsList**
> List&lt;Brand&gt; brandsList()

List Brands

Retrieve all brands associated with the current business context.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BrandsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BrandsApi apiInstance = new BrandsApi(defaultClient);
    try {
      List<Brand> result = apiInstance.brandsList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandsApi#brandsList");
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

[**List&lt;Brand&gt;**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of brands successfully retrieved. |  -  |

<a id="brandsUpdate"></a>
# **brandsUpdate**
> Brand brandsUpdate(id, brandUpdate)

Update Brand

Update website, logo, description, or statement descriptors of a brand.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.BrandsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    BrandsApi apiInstance = new BrandsApi(defaultClient);
    String id = "brd_123"; // String | The brand ID to update
    BrandUpdate brandUpdate = new BrandUpdate(); // BrandUpdate | 
    try {
      Brand result = apiInstance.brandsUpdate(id, brandUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandsApi#brandsUpdate");
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
| **id** | **String**| The brand ID to update | |
| **brandUpdate** | [**BrandUpdate**](BrandUpdate.md)|  | |

### Return type

[**Brand**](Brand.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Brand settings updated successfully. |  -  |

