# GitHubIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**githubGetInstallUrl**](GitHubIntegrationApi.md#githubGetInstallUrl) | **GET** /v1/github/install | Get GitHub App Installation URL |
| [**githubListRepos**](GitHubIntegrationApi.md#githubListRepos) | **GET** /v1/github/repos | List Available GitHub Repositories |


<a id="githubGetInstallUrl"></a>
# **githubGetInstallUrl**
> githubGetInstallUrl(productId)

Get GitHub App Installation URL

Generates the URL to install the system-wide GitHub App onto the merchant&#39;s GitHub account/org.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.GitHubIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    GitHubIntegrationApi apiInstance = new GitHubIntegrationApi(defaultClient);
    String productId = "productId_example"; // String | Optional Product ID to redirect back to after installation
    try {
      apiInstance.githubGetInstallUrl(productId);
    } catch (ApiException e) {
      System.err.println("Exception when calling GitHubIntegrationApi#githubGetInstallUrl");
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
| **productId** | **String**| Optional Product ID to redirect back to after installation | [optional] |

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
| **200** | Returns the generated installation URL. |  -  |

<a id="githubListRepos"></a>
# **githubListRepos**
> List&lt;GithubReposResponseDto&gt; githubListRepos()

List Available GitHub Repositories

Retrieves all repositories accessible by the merchant&#39;s installed GitHub App.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.auth.*;
import com.solifyn.models.*;
import com.solifyn.api.GitHubIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    GitHubIntegrationApi apiInstance = new GitHubIntegrationApi(defaultClient);
    try {
      List<GithubReposResponseDto> result = apiInstance.githubListRepos();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GitHubIntegrationApi#githubListRepos");
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

[**List&lt;GithubReposResponseDto&gt;**](GithubReposResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of repositories. |  -  |

