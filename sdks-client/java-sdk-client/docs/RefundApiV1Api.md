# RefundApiV1Api

All URIs are relative to *https://ressarcimento.opbkdev.smartfylabs.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**findNotificationById**](RefundApiV1Api.md#findNotificationById) | **GET** /apis/v1/refund/notifications/{processId} | Operação de consulta de processos de transações
[**healthcheck**](RefundApiV1Api.md#healthcheck) | **GET** /apis/v1/refund/notifications/healthcheck | Operação de consulta de monitoramento de processos de transações
[**notification**](RefundApiV1Api.md#notification) | **POST** /apis/v1/refund/notifications/ | Operação de registro unitário de transação 
[**notifications**](RefundApiV1Api.md#notifications) | **PATCH** /apis/v1/refund/notifications/ | Operação de registro em massa de uma transação

<a name="findNotificationById"></a>
# **findNotificationById**
> RefundProcess findNotificationById(processId)

Operação de consulta de processos de transações

Método da API de Consulta de processos de transações de APIs do Open Banking Brasil. O sistema utilizará essas informações para consultar processos que podem ter uma ou mais transações dentro da plataformas dos participantes. &lt;br&gt; Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RefundApiV1Api;


RefundApiV1Api apiInstance = new RefundApiV1Api();
String processId = "processId_example"; // String | 
try {
    RefundProcess result = apiInstance.findNotificationById(processId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RefundApiV1Api#findNotificationById");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **processId** | **String**|  |

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="healthcheck"></a>
# **healthcheck**
> RefundProcess healthcheck()

Operação de consulta de monitoramento de processos de transações

Método da API de Consulta de Monitoramento de processos de transações para verificar o status das APIs do Open Banking Brasil.O sistema utilizará essas informações para monitorar os processos e transações dentro das plataformas dos participantes. &lt;br&gt; Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RefundApiV1Api;


RefundApiV1Api apiInstance = new RefundApiV1Api();
try {
    RefundProcess result = apiInstance.healthcheck();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RefundApiV1Api#healthcheck");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="notification"></a>
# **notification**
> RefundProcess notification(body)

Operação de registro unitário de transação 

Método da API de Reporte unitário de consumo de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. &lt;br&gt; Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RefundApiV1Api;


RefundApiV1Api apiInstance = new RefundApiV1Api();
RefundNotification body = new RefundNotification(); // RefundNotification | 
try {
    RefundProcess result = apiInstance.notification(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RefundApiV1Api#notification");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**RefundNotification**](RefundNotification.md)|  |

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="notifications"></a>
# **notifications**
> RefundProcess notifications(body)

Operação de registro em massa de uma transação

Método da API de Reporte de atualização em massa de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. &lt;br&gt; Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RefundApiV1Api;


RefundApiV1Api apiInstance = new RefundApiV1Api();
List<RefundNotification> body = Arrays.asList(new RefundNotification()); // List<RefundNotification> | 
try {
    RefundProcess result = apiInstance.notifications(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RefundApiV1Api#notifications");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**List&lt;RefundNotification&gt;**](RefundNotification.md)|  |

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

