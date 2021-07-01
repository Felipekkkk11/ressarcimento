# {{classname}}

All URIs are relative to *https://ressarcimento.opbkdev.smartfylabs.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**FindNotificationById**](RefundAPIV1Api.md#FindNotificationById) | **Get** /apis/v1/refund/notifications/{processId} | Operação de consulta de processos de transações
[**Healthcheck**](RefundAPIV1Api.md#Healthcheck) | **Get** /apis/v1/refund/notifications/healthcheck | Operação de consulta de monitoramento de processos de transações
[**Notification**](RefundAPIV1Api.md#Notification) | **Post** /apis/v1/refund/notifications/ | Operação de registro unitário de transação 
[**Notifications**](RefundAPIV1Api.md#Notifications) | **Patch** /apis/v1/refund/notifications/ | Operação de registro em massa de uma transação

# **FindNotificationById**
> RefundProcess FindNotificationById(ctx, processId)
Operação de consulta de processos de transações

Método da API de Consulta de processos de transações de APIs do Open Banking Brasil. O sistema utilizará essas informações para consultar processos que podem ter uma ou mais transações dentro da plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **processId** | **string**|  | 

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Healthcheck**
> RefundProcess Healthcheck(ctx, )
Operação de consulta de monitoramento de processos de transações

Método da API de Consulta de Monitoramento de processos de transações para verificar o status das APIs do Open Banking Brasil.O sistema utilizará essas informações para monitorar os processos e transações dentro das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Notification**
> RefundProcess Notification(ctx, body)
Operação de registro unitário de transação 

Método da API de Reporte unitário de consumo de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**RefundNotification**](RefundNotification.md)|  | 

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Notifications**
> RefundProcess Notifications(ctx, body)
Operação de registro em massa de uma transação

Método da API de Reporte de atualização em massa de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**[]RefundNotification**](RefundNotification.md)|  | 

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

