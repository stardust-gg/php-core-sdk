# Stardust\Core\TemplateEndpointsApi

All URIs are relative to https://core-api.stardust.gg/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**templateCountGet()**](TemplateEndpointsApi.md#templateCountGet) | **GET** /template/count | Get Template Count |
| [**templateCreatePost()**](TemplateEndpointsApi.md#templateCreatePost) | **POST** /template/create | Create Template |
| [**templateGetAllGet()**](TemplateEndpointsApi.md#templateGetAllGet) | **GET** /template/get-all | Get All Templates |
| [**templateGetGet()**](TemplateEndpointsApi.md#templateGetGet) | **GET** /template/get | Get Template |
| [**templateGetTokensGet()**](TemplateEndpointsApi.md#templateGetTokensGet) | **GET** /template/get-tokens | Get Template Tokens |
| [**templateMutatePut()**](TemplateEndpointsApi.md#templateMutatePut) | **PUT** /template/mutate | Mutate Template |
| [**templatePropsRemoveDelete()**](TemplateEndpointsApi.md#templatePropsRemoveDelete) | **DELETE** /template/props-remove | Remove Template Property |
| [**templateRemoveDelete()**](TemplateEndpointsApi.md#templateRemoveDelete) | **DELETE** /template/remove | Remove Template |


## `templateCountGet()`

```php
templateCountGet($filter): \Stardust\Core\Stardust\Core\Model\SDTemplateCountResponse
```

Get Template Count

Get a Template's Count Within a Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$filter = 'filter_example'; // string | Find a substring within the Template name field

try {
    $result = $apiInstance->templateCountGet($filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templateCountGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **filter** | **string**| Find a substring within the Template name field | [optional] |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDTemplateCountResponse**](../Model/SDTemplateCountResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templateCreatePost()`

```php
templateCreatePost($sd_template_create_request): \Stardust\Core\Stardust\Core\Model\SDTemplateCreateResponse
```

Create Template

Adds a New Token Template that lets Players Acquire that Token using the Token/Mint Endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_template_create_request = new \Stardust\Core\Stardust\Core\Model\SDTemplateCreateRequest(); // \Stardust\Core\Stardust\Core\Model\SDTemplateCreateRequest

try {
    $result = $apiInstance->templateCreatePost($sd_template_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templateCreatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_template_create_request** | [**\Stardust\Core\Stardust\Core\Model\SDTemplateCreateRequest**](../Model/SDTemplateCreateRequest.md)|  | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDTemplateCreateResponse**](../Model/SDTemplateCreateResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templateGetAllGet()`

```php
templateGetAllGet($start, $limit, $filter): \Stardust\Core\Stardust\Core\Model\SDTemplateGetAllResponse[]
```

Get All Templates

Get All of the Templates Within a Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start = 'start_example'; // string | position in list
$limit = 'limit_example'; // string | maximum templates returned in list
$filter = 'filter_example'; // string | Find a substring within the Template name field

try {
    $result = $apiInstance->templateGetAllGet($start, $limit, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templateGetAllGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **start** | **string**| position in list | |
| **limit** | **string**| maximum templates returned in list | |
| **filter** | **string**| Find a substring within the Template name field | [optional] |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDTemplateGetAllResponse[]**](../Model/SDTemplateGetAllResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templateGetGet()`

```php
templateGetGet($template_id): \Stardust\Core\Stardust\Core\Model\SDTemplateGetResponse
```

Get Template

Get the Details of a Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string | Template Id such as 3589)

try {
    $result = $apiInstance->templateGetGet($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templateGetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**| Template Id such as 3589) | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDTemplateGetResponse**](../Model/SDTemplateGetResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templateGetTokensGet()`

```php
templateGetTokensGet($template_id, $start, $limit, $include_deleted): \Stardust\Core\Stardust\Core\Model\SDTemplateGetTokensResponse[]
```

Get Template Tokens

Get a List of All Minted Tokens from a Given Template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string | The ID of the Template
$start = 'start_example'; // string | position in list
$limit = 'limit_example'; // string | maximum templates returned in list
$include_deleted = 'include_deleted_example'; // string | If true tokens from deleted players are included in the response

try {
    $result = $apiInstance->templateGetTokensGet($template_id, $start, $limit, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templateGetTokensGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**| The ID of the Template | |
| **start** | **string**| position in list | [optional] |
| **limit** | **string**| maximum templates returned in list | [optional] |
| **include_deleted** | **string**| If true tokens from deleted players are included in the response | [optional] |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDTemplateGetTokensResponse[]**](../Model/SDTemplateGetTokensResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templateMutatePut()`

```php
templateMutatePut($sd_template_mutate_request): object
```

Mutate Template

Mutates a Property of a Template, Which in Turn will Affect the Inherited Property on All of the Tokens Created from this Template (via token/mint)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_template_mutate_request = new \Stardust\Core\Stardust\Core\Model\SDTemplateMutateRequest(); // \Stardust\Core\Stardust\Core\Model\SDTemplateMutateRequest

try {
    $result = $apiInstance->templateMutatePut($sd_template_mutate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templateMutatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_template_mutate_request** | [**\Stardust\Core\Stardust\Core\Model\SDTemplateMutateRequest**](../Model/SDTemplateMutateRequest.md)|  | |

### Return type

**object**

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templatePropsRemoveDelete()`

```php
templatePropsRemoveDelete($template_id, $props): object
```

Remove Template Property

Removes a Templates Property from Your Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string | Template Id returned from template/create (ex. 5)
$props = 'props_example'; // string | Stringify Array of template mutable property names ex: '[\"exp\", \"health\"]' }

try {
    $result = $apiInstance->templatePropsRemoveDelete($template_id, $props);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templatePropsRemoveDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**| Template Id returned from template/create (ex. 5) | |
| **props** | **string**| Stringify Array of template mutable property names ex: &#39;[\&quot;exp\&quot;, \&quot;health\&quot;]&#39; } | |

### Return type

**object**

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `templateRemoveDelete()`

```php
templateRemoveDelete($template_id): object
```

Remove Template

Removes a Template from Your Game. If Players have Instances of this Template from the token/mint Command, Their Tokens will NOT be Removed

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TemplateEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 'template_id_example'; // string | Template Id returned from template/create (ex. 5)

try {
    $result = $apiInstance->templateRemoveDelete($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateEndpointsApi->templateRemoveDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **string**| Template Id returned from template/create (ex. 5) | |

### Return type

**object**

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
