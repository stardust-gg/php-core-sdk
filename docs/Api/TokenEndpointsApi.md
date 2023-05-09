# Stardust\Core\TokenEndpointsApi

All URIs are relative to https://core-api.stardust.gg/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**tokenBurnPost()**](TokenEndpointsApi.md#tokenBurnPost) | **POST** /token/burn | Burn Token |
| [**tokenGetGet()**](TokenEndpointsApi.md#tokenGetGet) | **GET** /token/get | Get Token |
| [**tokenMintBulkPost()**](TokenEndpointsApi.md#tokenMintBulkPost) | **POST** /token/mint-bulk | Mint Tokens |
| [**tokenMutatePut()**](TokenEndpointsApi.md#tokenMutatePut) | **PUT** /token/mutate | Mutate Token |
| [**tokenPropsRemoveDelete()**](TokenEndpointsApi.md#tokenPropsRemoveDelete) | **DELETE** /token/props-remove | Remove Token Property |
| [**tokenTransferPost()**](TokenEndpointsApi.md#tokenTransferPost) | **POST** /token/transfer | Transfer Tokens |
| [**tokenWithdrawPost()**](TokenEndpointsApi.md#tokenWithdrawPost) | **POST** /token/withdraw | Withdraw Token |


## `tokenBurnPost()`

```php
tokenBurnPost($sd_token_burn_request): object
```

Burn Token

Burns token on-chain. Cannot be reversed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TokenEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_token_burn_request = new \Stardust\Core\Stardust\Core\Model\SDTokenBurnRequest(); // \Stardust\Core\Stardust\Core\Model\SDTokenBurnRequest

try {
    $result = $apiInstance->tokenBurnPost($sd_token_burn_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenEndpointsApi->tokenBurnPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_token_burn_request** | [**\Stardust\Core\Stardust\Core\Model\SDTokenBurnRequest**](../Model/SDTokenBurnRequest.md)|  | |

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

## `tokenGetGet()`

```php
tokenGetGet($token_ids): \Stardust\Core\Stardust\Core\Model\SDTokenGetResponse[]
```

Get Token

Some of the details of this token are based upon the Template that it was created from (using token/mint)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TokenEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token_ids = 'token_ids_example'; // string | Stringify Array of token ids (ex. '[3589, 3580]')

try {
    $result = $apiInstance->tokenGetGet($token_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenEndpointsApi->tokenGetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token_ids** | **string**| Stringify Array of token ids (ex. &#39;[3589, 3580]&#39;) | |

### Return type

[**\Stardust\Core\Stardust\Core\Model\SDTokenGetResponse[]**](../Model/SDTokenGetResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `tokenMintBulkPost()`

```php
tokenMintBulkPost($sd_token_mint_bulk_request): int[]
```

Mint Tokens

Mint tokens to a player

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TokenEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_token_mint_bulk_request = new \Stardust\Core\Stardust\Core\Model\SDTokenMintBulkRequest(); // \Stardust\Core\Stardust\Core\Model\SDTokenMintBulkRequest

try {
    $result = $apiInstance->tokenMintBulkPost($sd_token_mint_bulk_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenEndpointsApi->tokenMintBulkPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_token_mint_bulk_request** | [**\Stardust\Core\Stardust\Core\Model\SDTokenMintBulkRequest**](../Model/SDTokenMintBulkRequest.md)|  | |

### Return type

**int[]**

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `tokenMutatePut()`

```php
tokenMutatePut($sd_token_mutate_request): object
```

Mutate Token

Mutates a Property of a Token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TokenEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_token_mutate_request = new \Stardust\Core\Stardust\Core\Model\SDTokenMutateRequest(); // \Stardust\Core\Stardust\Core\Model\SDTokenMutateRequest

try {
    $result = $apiInstance->tokenMutatePut($sd_token_mutate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenEndpointsApi->tokenMutatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_token_mutate_request** | [**\Stardust\Core\Stardust\Core\Model\SDTokenMutateRequest**](../Model/SDTokenMutateRequest.md)|  | |

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

## `tokenPropsRemoveDelete()`

```php
tokenPropsRemoveDelete($token_id, $props): object
```

Remove Token Property

Removes a Tokens Property from Your Game

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TokenEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token_id = 'token_id_example'; // string | Token Id returned from token/create (ex. 5)
$props = 'props_example'; // string | Stringify Array of token mutable property names ex: '[\"exp\", \"health\"]' }

try {
    $result = $apiInstance->tokenPropsRemoveDelete($token_id, $props);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenEndpointsApi->tokenPropsRemoveDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **token_id** | **string**| Token Id returned from token/create (ex. 5) | |
| **props** | **string**| Stringify Array of token mutable property names ex: &#39;[\&quot;exp\&quot;, \&quot;health\&quot;]&#39; } | |

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

## `tokenTransferPost()`

```php
tokenTransferPost($sd_token_transfer_request): object
```

Transfer Tokens

Use this Endpoint to Facilitate Moving Tokens from one Player to Another

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TokenEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_token_transfer_request = new \Stardust\Core\Stardust\Core\Model\SDTokenTransferRequest(); // \Stardust\Core\Stardust\Core\Model\SDTokenTransferRequest

try {
    $result = $apiInstance->tokenTransferPost($sd_token_transfer_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenEndpointsApi->tokenTransferPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_token_transfer_request** | [**\Stardust\Core\Stardust\Core\Model\SDTokenTransferRequest**](../Model/SDTokenTransferRequest.md)|  | |

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

## `tokenWithdrawPost()`

```php
tokenWithdrawPost($sd_token_withdraw_request): object
```

Withdraw Token

Withdraw tokens from a Stardust Wallet

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Stardust\Core\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new Stardust\Core\Api\TokenEndpointsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sd_token_withdraw_request = new \Stardust\Core\Stardust\Core\Model\SDTokenWithdrawRequest(); // \Stardust\Core\Stardust\Core\Model\SDTokenWithdrawRequest

try {
    $result = $apiInstance->tokenWithdrawPost($sd_token_withdraw_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenEndpointsApi->tokenWithdrawPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sd_token_withdraw_request** | [**\Stardust\Core\Stardust\Core\Model\SDTokenWithdrawRequest**](../Model/SDTokenWithdrawRequest.md)|  | |

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
