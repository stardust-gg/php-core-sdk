# Stardust\Core\HealthEndpointsApi

All URIs are relative to https://core-api.stardust.gg/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**healthGet()**](HealthEndpointsApi.md#healthGet) | **GET** /health | Get Health |


## `healthGet()`

```php
healthGet(): \Stardust\Core\Stardust\Core\Model\SDHealthResponse
```

Get Health

Get system health info

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Stardust\Core\Api\HealthEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->healthGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthEndpointsApi->healthGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDHealthResponse**](../Model/SDHealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
