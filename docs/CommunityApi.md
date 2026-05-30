# CommunityApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**communityControllerCreatePost**](CommunityApi.md#communityControllerCreatePost) | **POST** /v1/community/posts |  |
| [**communityControllerDeletePost**](CommunityApi.md#communityControllerDeletePost) | **DELETE** /v1/community/posts/{id} |  |
| [**communityControllerGetPosts**](CommunityApi.md#communityControllerGetPosts) | **GET** /v1/community/posts |  |
| [**communityControllerLikePost**](CommunityApi.md#communityControllerLikePost) | **PATCH** /v1/community/posts/{id}/like |  |
| [**communityControllerReportPost**](CommunityApi.md#communityControllerReportPost) | **POST** /v1/community/posts/{id}/report |  |
| [**communityControllerSharePost**](CommunityApi.md#communityControllerSharePost) | **PATCH** /v1/community/posts/{id}/share |  |
| [**communityControllerUnlikePost**](CommunityApi.md#communityControllerUnlikePost) | **PATCH** /v1/community/posts/{id}/unlike |  |
| [**communityControllerUpdatePost**](CommunityApi.md#communityControllerUpdatePost) | **PATCH** /v1/community/posts/{id} |  |


<a id="communityControllerCreatePost"></a>
# **communityControllerCreatePost**
> communityControllerCreatePost()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    try {
      apiInstance.communityControllerCreatePost();
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerCreatePost");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="communityControllerDeletePost"></a>
# **communityControllerDeletePost**
> communityControllerDeletePost(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.communityControllerDeletePost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerDeletePost");
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
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="communityControllerGetPosts"></a>
# **communityControllerGetPosts**
> communityControllerGetPosts()



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    try {
      apiInstance.communityControllerGetPosts();
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerGetPosts");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="communityControllerLikePost"></a>
# **communityControllerLikePost**
> communityControllerLikePost(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.communityControllerLikePost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerLikePost");
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
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="communityControllerReportPost"></a>
# **communityControllerReportPost**
> communityControllerReportPost(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.communityControllerReportPost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerReportPost");
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
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

<a id="communityControllerSharePost"></a>
# **communityControllerSharePost**
> communityControllerSharePost(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.communityControllerSharePost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerSharePost");
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
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="communityControllerUnlikePost"></a>
# **communityControllerUnlikePost**
> communityControllerUnlikePost(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.communityControllerUnlikePost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerUnlikePost");
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
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

<a id="communityControllerUpdatePost"></a>
# **communityControllerUpdatePost**
> communityControllerUpdatePost(id)



### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.CommunityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8000");

    CommunityApi apiInstance = new CommunityApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.communityControllerUpdatePost(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityApi#communityControllerUpdatePost");
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
| **id** | **String**|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

