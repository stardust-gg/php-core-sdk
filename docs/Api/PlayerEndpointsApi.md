# Stardust\Core\PlayerEndpointsApi

All URIs are relative to https://core-api.stardust.gg/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**playerCountGet()**](PlayerEndpointsApi.md#playerCountGet) | **GET** /player/count | Get Player Count |
| [**playerCreatePost()**](PlayerEndpointsApi.md#playerCreatePost) | **POST** /player/create | Create Player |
| [**playerGetAllGet()**](PlayerEndpointsApi.md#playerGetAllGet) | **GET** /player/get-all | Get All Players |
| [**playerGetGet()**](PlayerEndpointsApi.md#playerGetGet) | **GET** /player/get | Get Player |
| [**playerGetIdGet()**](PlayerEndpointsApi.md#playerGetIdGet) | **GET** /player/get-id | Get Player ID |
| [**playerGetIdsGet()**](PlayerEndpointsApi.md#playerGetIdsGet) | **GET** /player/get-ids | Get All Player IDs |
| [**playerGetInventoryGet()**](PlayerEndpointsApi.md#playerGetInventoryGet) | **GET** /player/get-inventory | Get Player Inventory |
| [**playerMutatePut()**](PlayerEndpointsApi.md#playerMutatePut) | **PUT** /player/mutate | Mutate Player |
| [**playerRemoveDelete()**](PlayerEndpointsApi.md#playerRemoveDelete) | **DELETE** /player/remove | Remove Player |
| [**playerWalletGetGet()**](PlayerEndpointsApi.md#playerWalletGetGet) | **GET** /player/wallet-get | Get Player Wallet |
| [**playerWithdrawPost()**](PlayerEndpointsApi.md#playerWithdrawPost) | **POST** /player/withdraw | Withdraw From Player |


## `playerCountGet()`

```php
playerCountGet(): \Stardust\Core\Stardust\Core\Model\SDPlayerCountResponse
```

Get Player Count

Get Player count within a game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->playerCountGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerCountGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerCountResponse**](../Model/SDPlayerCountResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerCreatePost()`

```php
playerCreatePost($sd_player_create_request): \Stardust\Core\Stardust\Core\Model\SDPlayerCreateResponse
```

Create Player

Create a Player for a game. Returns their player id which can be used to reference them later in Stardust's system

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_player_create_request = new \Stardust\Core\Stardust\Core\Model\SDPlayerCreateRequest(); // \Stardust\Core\Stardust\Core\Model\SDPlayerCreateRequest

try {
    $result = $apiInstance->playerCreatePost($sd_player_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerCreatePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_player_create_request** | [**\Stardust\Core\Stardust\Core\Model\SDPlayerCreateRequest**](../Model/SDPlayerCreateRequest.md)|  | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerCreateResponse**](../Model/SDPlayerCreateResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerGetAllGet()`

```php
playerGetAllGet($start, $filter, $limit): \Stardust\Core\Stardust\Core\Model\SDPlayerGetAllResponse[]
```

Get All Players

Get the List of All Players in Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start = 'start_example'; // string | position in list
$filter = 'filter_example'; // string | Find a substring within the Player unique ID field
$limit = 'limit_example'; // string | maximum items returned in list

try {
    $result = $apiInstance->playerGetAllGet($start, $filter, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerGetAllGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **start** | **string**| position in list | [optional] |
| **filter** | **string**| Find a substring within the Player unique ID field | [optional] |
| **limit** | **string**| maximum items returned in list | [optional] |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerGetAllResponse[]**](../Model/SDPlayerGetAllResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerGetGet()`

```php
playerGetGet($player_id): \Stardust\Core\Stardust\Core\Model\SDPlayerGetResponse
```

Get Player

Get Details of a Player Within a Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$player_id = 'player_id_example'; // string | Player id

try {
    $result = $apiInstance->playerGetGet($player_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerGetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **player_id** | **string**| Player id | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerGetResponse**](../Model/SDPlayerGetResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerGetIdGet()`

```php
playerGetIdGet($unique_id): \Stardust\Core\Stardust\Core\Model\SDPlayerGetIdResponse
```

Get Player ID

Get a Player's ID via their Unique ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$unique_id = 'unique_id_example'; // string | Player's Unique ID

try {
    $result = $apiInstance->playerGetIdGet($unique_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerGetIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **unique_id** | **string**| Player&#39;s Unique ID | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerGetIdResponse**](../Model/SDPlayerGetIdResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerGetIdsGet()`

```php
playerGetIdsGet(): \Stardust\Core\Stardust\Core\Model\SDPlayerGetIdsResponse[]
```

Get All Player IDs

Get All Player IDs for a Given Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->playerGetIdsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerGetIdsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerGetIdsResponse[]**](../Model/SDPlayerGetIdsResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerGetInventoryGet()`

```php
playerGetInventoryGet($player_id, $start, $token_ids, $limit): \Stardust\Core\Stardust\Core\Model\SDPlayerGetInventoryResponse[]
```

Get Player Inventory

Get a players inventory and all the items it holds

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$player_id = 'player_id_example'; // string | Player id
$start = 'start_example'; // string | position in list
$token_ids = 'token_ids_example'; // string | Comma-Separated String of token ids (ex. '3589, 3580')
$limit = 'limit_example'; // string | maximum items returned in list

try {
    $result = $apiInstance->playerGetInventoryGet($player_id, $start, $token_ids, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerGetInventoryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **player_id** | **string**| Player id | |
| **start** | **string**| position in list | [optional] |
| **token_ids** | **string**| Comma-Separated String of token ids (ex. &#39;3589, 3580&#39;) | [optional] |
| **limit** | **string**| maximum items returned in list | [optional] |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerGetInventoryResponse[]**](../Model/SDPlayerGetInventoryResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerMutatePut()`

```php
playerMutatePut($sd_player_mutate_request): object
```

Mutate Player

Change player data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_player_mutate_request = new \Stardust\Core\Stardust\Core\Model\SDPlayerMutateRequest(); // \Stardust\Core\Stardust\Core\Model\SDPlayerMutateRequest

try {
    $result = $apiInstance->playerMutatePut($sd_player_mutate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerMutatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_player_mutate_request** | [**\Stardust\Core\Stardust\Core\Model\SDPlayerMutateRequest**](../Model/SDPlayerMutateRequest.md)|  | |

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

## `playerRemoveDelete()`

```php
playerRemoveDelete($player_id): object
```

Remove Player

Removes (hides) a player from your game. This is not permanent.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$player_id = 'player_id_example'; // string | Player Id returned from player/create a UUID, i.e. 802760b0-2bb5-4fba-9237-895ed02cf8d8

try {
    $result = $apiInstance->playerRemoveDelete($player_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerRemoveDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **player_id** | **string**| Player Id returned from player/create a UUID, i.e. 802760b0-2bb5-4fba-9237-895ed02cf8d8 | |

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

## `playerWalletGetGet()`

```php
playerWalletGetGet($player_id): \Stardust\Core\Stardust\Core\Model\SDPlayerWalletGetResponse
```

Get Player Wallet

Get player's wallet within a game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$player_id = 'player_id_example'; // string | Player id

try {
    $result = $apiInstance->playerWalletGetGet($player_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerWalletGetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **player_id** | **string**| Player id | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDPlayerWalletGetResponse**](../Model/SDPlayerWalletGetResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `playerWithdrawPost()`

```php
playerWithdrawPost($sd_player_withdraw_request): object
```

Withdraw From Player

Withdraw a Player's Tokens from their Stardust Wallet

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\PlayerEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_player_withdraw_request = new \Stardust\Core\Stardust\Core\Model\SDPlayerWithdrawRequest(); // \Stardust\Core\Stardust\Core\Model\SDPlayerWithdrawRequest

try {
    $result = $apiInstance->playerWithdrawPost($sd_player_withdraw_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlayerEndpointsApi->playerWithdrawPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_player_withdraw_request** | [**\Stardust\Core\Stardust\Core\Model\SDPlayerWithdrawRequest**](../Model/SDPlayerWithdrawRequest.md)|  | |

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
