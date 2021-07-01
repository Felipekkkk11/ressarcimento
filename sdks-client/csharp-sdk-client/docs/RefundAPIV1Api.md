# IO.Swagger.Api.RefundAPIV1Api

All URIs are relative to *https://ressarcimento.opbkdev.smartfylabs.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**FindNotificationById**](RefundAPIV1Api.md#findnotificationbyid) | **GET** /apis/v1/refund/notifications/{processId} | Operação de consulta de processos de transações
[**Healthcheck**](RefundAPIV1Api.md#healthcheck) | **GET** /apis/v1/refund/notifications/healthcheck | Operação de consulta de monitoramento de processos de transações
[**Notification**](RefundAPIV1Api.md#notification) | **POST** /apis/v1/refund/notifications/ | Operação de registro unitário de transação 
[**Notifications**](RefundAPIV1Api.md#notifications) | **PATCH** /apis/v1/refund/notifications/ | Operação de registro em massa de uma transação

<a name="findnotificationbyid"></a>
# **FindNotificationById**
> RefundProcess FindNotificationById (string processId)

Operação de consulta de processos de transações

Método da API de Consulta de processos de transações de APIs do Open Banking Brasil. O sistema utilizará essas informações para consultar processos que podem ter uma ou mais transações dentro da plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class FindNotificationByIdExample
    {
        public void main()
        {
            var apiInstance = new RefundAPIV1Api();
            var processId = processId_example;  // string | 

            try
            {
                // Operação de consulta de processos de transações
                RefundProcess result = apiInstance.FindNotificationById(processId);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RefundAPIV1Api.FindNotificationById: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **processId** | **string**|  | 

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="healthcheck"></a>
# **Healthcheck**
> RefundProcess Healthcheck ()

Operação de consulta de monitoramento de processos de transações

Método da API de Consulta de Monitoramento de processos de transações para verificar o status das APIs do Open Banking Brasil.O sistema utilizará essas informações para monitorar os processos e transações dentro das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class HealthcheckExample
    {
        public void main()
        {
            var apiInstance = new RefundAPIV1Api();

            try
            {
                // Operação de consulta de monitoramento de processos de transações
                RefundProcess result = apiInstance.Healthcheck();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RefundAPIV1Api.Healthcheck: " + e.Message );
            }
        }
    }
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="notification"></a>
# **Notification**
> RefundProcess Notification (RefundNotification body)

Operação de registro unitário de transação 

Método da API de Reporte unitário de consumo de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class NotificationExample
    {
        public void main()
        {
            var apiInstance = new RefundAPIV1Api();
            var body = new RefundNotification(); // RefundNotification | 

            try
            {
                // Operação de registro unitário de transação 
                RefundProcess result = apiInstance.Notification(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RefundAPIV1Api.Notification: " + e.Message );
            }
        }
    }
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="notifications"></a>
# **Notifications**
> RefundProcess Notifications (List<RefundNotification> body)

Operação de registro em massa de uma transação

Método da API de Reporte de atualização em massa de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class NotificationsExample
    {
        public void main()
        {
            var apiInstance = new RefundAPIV1Api();
            var body = new List<RefundNotification>(); // List<RefundNotification> | 

            try
            {
                // Operação de registro em massa de uma transação
                RefundProcess result = apiInstance.Notifications(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RefundAPIV1Api.Notifications: " + e.Message );
            }
        }
    }
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
