# DiscordIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**discordGetInstallUrl**](DiscordIntegrationApi.md#discordGetInstallUrl) | **GET** /v1/discord/install | Get Discord Bot Installation URL |
| [**discordListRoles**](DiscordIntegrationApi.md#discordListRoles) | **GET** /v1/discord/roles | List Guild Discord Roles |


<a id="discordGetInstallUrl"></a>
# **discordGetInstallUrl**
> discordGetInstallUrl(productId)

Get Discord Bot Installation URL

Generates the URL to invite the system-wide Discord Bot onto the merchant&#39;s Discord server.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DiscordIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    DiscordIntegrationApi apiInstance = new DiscordIntegrationApi(defaultClient);
    String productId = "productId_example"; // String | Optional Product ID to redirect back to after installation
    try {
      apiInstance.discordGetInstallUrl(productId);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscordIntegrationApi#discordGetInstallUrl");
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

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns the generated installation URL. |  -  |

<a id="discordListRoles"></a>
# **discordListRoles**
> List&lt;DiscordRolesResponseDto&gt; discordListRoles()

List Guild Discord Roles

Retrieves all roles available in the connected merchant&#39;s Discord server/guild.

### Example
```java
// Import classes:
import com.solifyn.ApiClient;
import com.solifyn.ApiException;
import com.solifyn.Configuration;
import com.solifyn.models.*;
import com.solifyn.api.DiscordIntegrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.solifyn.com");

    DiscordIntegrationApi apiInstance = new DiscordIntegrationApi(defaultClient);
    try {
      List<DiscordRolesResponseDto> result = apiInstance.discordListRoles();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscordIntegrationApi#discordListRoles");
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

[**List&lt;DiscordRolesResponseDto&gt;**](DiscordRolesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of server roles. |  -  |

