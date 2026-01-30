# AuthApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**authControllerExchangeToken**](#authcontrollerexchangetoken) | **POST** /auth/google/{token} | Exchange token|
|[**authControllerForgetPassword**](#authcontrollerforgetpassword) | **POST** /auth/forget-password | Forget password initiate|
|[**authControllerForgetPasswordVerification**](#authcontrollerforgetpasswordverification) | **POST** /auth/forget-password/verification | Forget password verification|
|[**authControllerLogin**](#authcontrollerlogin) | **POST** /auth/login | Login to the application|
|[**authControllerOAuthLogin**](#authcontrolleroauthlogin) | **POST** /auth/login/oauth | Login with OAuth apps|
|[**authControllerRefreshToken**](#authcontrollerrefreshtoken) | **POST** /auth/google/refresh/{token} | Refresh Google access token|
|[**authControllerResetPassword**](#authcontrollerresetpassword) | **POST** /auth/reset-password | Forget password initiate|
|[**authControllerSignup**](#authcontrollersignup) | **POST** /auth/signup | Signup in the application|

# **authControllerExchangeToken**
> object authControllerExchangeToken()


### Example

```typescript
import {
    AuthApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let token: string; // (default to undefined)

const { status, data } = await apiInstance.authControllerExchangeToken(
    token
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token** | [**string**] |  | defaults to undefined|


### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authControllerForgetPassword**
> ForgetPasswordResponseDTO authControllerForgetPassword(forgetPasswordRequestDTO)


### Example

```typescript
import {
    AuthApi,
    Configuration,
    ForgetPasswordRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let forgetPasswordRequestDTO: ForgetPasswordRequestDTO; //

const { status, data } = await apiInstance.authControllerForgetPassword(
    forgetPasswordRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **forgetPasswordRequestDTO** | **ForgetPasswordRequestDTO**|  | |


### Return type

**ForgetPasswordResponseDTO**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authControllerForgetPasswordVerification**
> ForgetPasswordVerificationResponseDTO authControllerForgetPasswordVerification(forgetPasswordVerificationRequestDTO)


### Example

```typescript
import {
    AuthApi,
    Configuration,
    ForgetPasswordVerificationRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let forgetPasswordVerificationRequestDTO: ForgetPasswordVerificationRequestDTO; //

const { status, data } = await apiInstance.authControllerForgetPasswordVerification(
    forgetPasswordVerificationRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **forgetPasswordVerificationRequestDTO** | **ForgetPasswordVerificationRequestDTO**|  | |


### Return type

**ForgetPasswordVerificationResponseDTO**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authControllerLogin**
> LoginResponseDTO authControllerLogin(loginRequestDTO)


### Example

```typescript
import {
    AuthApi,
    Configuration,
    LoginRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let loginRequestDTO: LoginRequestDTO; //

const { status, data } = await apiInstance.authControllerLogin(
    loginRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **loginRequestDTO** | **LoginRequestDTO**|  | |


### Return type

**LoginResponseDTO**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authControllerOAuthLogin**
> LoginResponseDTO authControllerOAuthLogin(oAuthLoginRequestDTO)


### Example

```typescript
import {
    AuthApi,
    Configuration,
    OAuthLoginRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let oAuthLoginRequestDTO: OAuthLoginRequestDTO; //

const { status, data } = await apiInstance.authControllerOAuthLogin(
    oAuthLoginRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **oAuthLoginRequestDTO** | **OAuthLoginRequestDTO**|  | |


### Return type

**LoginResponseDTO**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authControllerRefreshToken**
> object authControllerRefreshToken()


### Example

```typescript
import {
    AuthApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let token: string; // (default to undefined)

const { status, data } = await apiInstance.authControllerRefreshToken(
    token
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token** | [**string**] |  | defaults to undefined|


### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authControllerResetPassword**
> BooleanResponseDTO authControllerResetPassword(resetPasswordRequestDTO)


### Example

```typescript
import {
    AuthApi,
    Configuration,
    ResetPasswordRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let resetPasswordRequestDTO: ResetPasswordRequestDTO; //

const { status, data } = await apiInstance.authControllerResetPassword(
    resetPasswordRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **resetPasswordRequestDTO** | **ResetPasswordRequestDTO**|  | |


### Return type

**BooleanResponseDTO**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authControllerSignup**
> SignupResponseDTO authControllerSignup(signupRequestDTO)


### Example

```typescript
import {
    AuthApi,
    Configuration,
    SignupRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new AuthApi(configuration);

let signupRequestDTO: SignupRequestDTO; //

const { status, data } = await apiInstance.authControllerSignup(
    signupRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **signupRequestDTO** | **SignupRequestDTO**|  | |


### Return type

**SignupResponseDTO**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

