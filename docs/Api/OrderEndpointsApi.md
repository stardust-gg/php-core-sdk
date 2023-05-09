# Stardust\Core\OrderEndpointsApi

All URIs are relative to https://core-api.stardust.gg/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**orderBuyPost()**](OrderEndpointsApi.md#orderBuyPost) | **POST** /order/buy | Buy Order |
| [**orderCancelDelete()**](OrderEndpointsApi.md#orderCancelDelete) | **DELETE** /order/cancel | Cancel Order |
| [**orderCreatePost()**](OrderEndpointsApi.md#orderCreatePost) | **POST** /order/create | Create Order |
| [**orderGetAllGet()**](OrderEndpointsApi.md#orderGetAllGet) | **GET** /order/get-all | Get All Orders |
| [**orderGetGet()**](OrderEndpointsApi.md#orderGetGet) | **GET** /order/get | Get Order |


## `orderBuyPost()`

```php
orderBuyPost($sd_order_buy_request): object
```

Buy Order

Buy a Order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\OrderEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_order_buy_request = new \Stardust\Core\Stardust\Core\Model\SDOrderBuyRequest(); // \Stardust\Core\Stardust\Core\Model\SDOrderBuyRequest

try {
    $result = $apiInstance->orderBuyPost($sd_order_buy_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderEndpointsApi->orderBuyPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_order_buy_request** | [**\Stardust\Core\Stardust\Core\Model\SDOrderBuyRequest**](../Model/SDOrderBuyRequest.md)|  | |

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

## `orderCancelDelete()`

```php
orderCancelDelete($order_id): object
```

Cancel Order

Cancels a Order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\OrderEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Order Id unsigned 32 bit integer

try {
    $result = $apiInstance->orderCancelDelete($order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderEndpointsApi->orderCancelDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **string**| Order Id unsigned 32 bit integer | |

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

## `orderCreatePost()`

```php
orderCreatePost($sd_order_create_request): \Stardust\Core\Stardust\Core\Model\SDOrderCreateResponse
```

Create Order

Adds a New Order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\OrderEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_order_create_request = new \Stardust\Core\Stardust\Core\Model\SDOrderCreateRequest(); // \Stardust\Core\Stardust\Core\Model\SDOrderCreateRequest

try {
    $result = $apiInstance->orderCreatePost($sd_order_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderEndpointsApi->orderCreatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_order_create_request** | [**\Stardust\Core\Stardust\Core\Model\SDOrderCreateRequest**](../Model/SDOrderCreateRequest.md)|  | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDOrderCreateResponse**](../Model/SDOrderCreateResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderGetAllGet()`

```php
orderGetAllGet($start, $limit, $player_id, $status): \Stardust\Core\Stardust\Core\Model\SDOrderGetAllResponse[]
```

Get All Orders

Get the List of Game Orders

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\OrderEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start = 'start_example'; // string | position in list
$limit = 'limit_example'; // string | maximum templates returned in list
$player_id = 'player_id_example'; // string | A Games PlayerId to filter by player
$status = 'status_example'; // string | State of the order to filter. Default is offer. ('offer', 'accepted', 'cancelled')

try {
    $result = $apiInstance->orderGetAllGet($start, $limit, $player_id, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderEndpointsApi->orderGetAllGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **start** | **string**| position in list | |
| **limit** | **string**| maximum templates returned in list | |
| **player_id** | **string**| A Games PlayerId to filter by player | [optional] |
| **status** | **string**| State of the order to filter. Default is offer. (&#39;offer&#39;, &#39;accepted&#39;, &#39;cancelled&#39;) | [optional] |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDOrderGetAllResponse[]**](../Model/SDOrderGetAllResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderGetGet()`

```php
orderGetGet($order_id): \Stardust\Core\Stardust\Core\Model\SDOrderGetResponse
```

Get Order

Get a Game Order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\OrderEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | An Order ID

try {
    $result = $apiInstance->orderGetGet($order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderEndpointsApi->orderGetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **string**| An Order ID | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDOrderGetResponse**](../Model/SDOrderGetResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
