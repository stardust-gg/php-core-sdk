# Stardust\Core\GameEndpointsApi

All URIs are relative to https://core-api.stardust.gg/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**gameGetGet()**](GameEndpointsApi.md#gameGetGet) | **GET** /game/get | Get Game |
| [**gameMutatePut()**](GameEndpointsApi.md#gameMutatePut) | **PUT** /game/mutate | Mutate Game |


## `gameGetGet()`

```php
gameGetGet(): \Stardust\Core\Stardust\Core\Model\SDGameGetResponse
```

Get Game

Get the Details of Your Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\GameEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->gameGetGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameEndpointsApi->gameGetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDGameGetResponse**](../Model/SDGameGetResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `gameMutatePut()`

```php
gameMutatePut($sd_game_mutate_request): object
```

Mutate Game

Change a games data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\GameEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_game_mutate_request = new \Stardust\Core\Stardust\Core\Model\SDGameMutateRequest(); // \Stardust\Core\Stardust\Core\Model\SDGameMutateRequest

try {
    $result = $apiInstance->gameMutatePut($sd_game_mutate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameEndpointsApi->gameMutatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_game_mutate_request** | [**\Stardust\Core\Stardust\Core\Model\SDGameMutateRequest**](../Model/SDGameMutateRequest.md)|  | |

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
