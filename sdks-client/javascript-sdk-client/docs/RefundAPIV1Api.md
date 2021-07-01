# PlataformaDeRessarcimentoDoOpenBankingBrasil.RefundAPIV1Api

All URIs are relative to *https://ressarcimento.opbkdev.smartfylabs.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**findNotificationById**](RefundAPIV1Api.md#findNotificationById) | **GET** /apis/v1/refund/notifications/{processId} | Operação de consulta de processos de transações
[**healthcheck**](RefundAPIV1Api.md#healthcheck) | **GET** /apis/v1/refund/notifications/healthcheck | Operação de consulta de monitoramento de processos de transações
[**notification**](RefundAPIV1Api.md#notification) | **POST** /apis/v1/refund/notifications/ | Operação de registro unitário de transação 
[**notifications**](RefundAPIV1Api.md#notifications) | **PATCH** /apis/v1/refund/notifications/ | Operação de registro em massa de uma transação

<a name="findNotificationById"></a>
# **findNotificationById**
> RefundProcess findNotificationById(processId)

Operação de consulta de processos de transações

Método da API de Consulta de processos de transações de APIs do Open Banking Brasil. O sistema utilizará essas informações para consultar processos que podem ter uma ou mais transações dentro da plataformas dos participantes. &lt;br&gt; Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```javascript
import {PlataformaDeRessarcimentoDoOpenBankingBrasil} from 'plataforma_de_ressarcimento_do_open_banking_brasil';

let apiInstance = new PlataformaDeRessarcimentoDoOpenBankingBrasil.RefundAPIV1Api();
let processId = "processId_example"; // String | 

apiInstance.findNotificationById(processId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
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
```javascript
import {PlataformaDeRessarcimentoDoOpenBankingBrasil} from 'plataforma_de_ressarcimento_do_open_banking_brasil';

let apiInstance = new PlataformaDeRessarcimentoDoOpenBankingBrasil.RefundAPIV1Api();
apiInstance.healthcheck((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
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
```javascript
import {PlataformaDeRessarcimentoDoOpenBankingBrasil} from 'plataforma_de_ressarcimento_do_open_banking_brasil';

let apiInstance = new PlataformaDeRessarcimentoDoOpenBankingBrasil.RefundAPIV1Api();
let body = new PlataformaDeRessarcimentoDoOpenBankingBrasil.RefundNotification(); // RefundNotification | 

apiInstance.notification(body, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
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
```javascript
import {PlataformaDeRessarcimentoDoOpenBankingBrasil} from 'plataforma_de_ressarcimento_do_open_banking_brasil';

let apiInstance = new PlataformaDeRessarcimentoDoOpenBankingBrasil.RefundAPIV1Api();
let body = [new PlataformaDeRessarcimentoDoOpenBankingBrasil.RefundNotification()]; // [RefundNotification] | 

apiInstance.notifications(body, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**[RefundNotification]**](RefundNotification.md)|  | 

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

