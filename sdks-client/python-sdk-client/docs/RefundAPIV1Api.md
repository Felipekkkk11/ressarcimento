# swagger_client.RefundAPIV1Api

All URIs are relative to *https://ressarcimento.opbkdev.smartfylabs.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**find_notification_by_id**](RefundAPIV1Api.md#find_notification_by_id) | **GET** /apis/v1/refund/notifications/{processId} | Operação de consulta de processos de transações
[**healthcheck**](RefundAPIV1Api.md#healthcheck) | **GET** /apis/v1/refund/notifications/healthcheck | Operação de consulta de monitoramento de processos de transações
[**notification**](RefundAPIV1Api.md#notification) | **POST** /apis/v1/refund/notifications/ | Operação de registro unitário de transação 
[**notifications**](RefundAPIV1Api.md#notifications) | **PATCH** /apis/v1/refund/notifications/ | Operação de registro em massa de uma transação

# **find_notification_by_id**
> RefundProcess find_notification_by_id(process_id)

Operação de consulta de processos de transações

Método da API de Consulta de processos de transações de APIs do Open Banking Brasil. O sistema utilizará essas informações para consultar processos que podem ter uma ou mais transações dentro da plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.RefundAPIV1Api()
process_id = 'process_id_example' # str | 

try:
    # Operação de consulta de processos de transações
    api_response = api_instance.find_notification_by_id(process_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RefundAPIV1Api->find_notification_by_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **process_id** | **str**|  | 

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **healthcheck**
> RefundProcess healthcheck()

Operação de consulta de monitoramento de processos de transações

Método da API de Consulta de Monitoramento de processos de transações para verificar o status das APIs do Open Banking Brasil.O sistema utilizará essas informações para monitorar os processos e transações dentro das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.RefundAPIV1Api()

try:
    # Operação de consulta de monitoramento de processos de transações
    api_response = api_instance.healthcheck()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RefundAPIV1Api->healthcheck: %s\n" % e)
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

# **notification**
> RefundProcess notification(body)

Operação de registro unitário de transação 

Método da API de Reporte unitário de consumo de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.RefundAPIV1Api()
body = swagger_client.RefundNotification() # RefundNotification | 

try:
    # Operação de registro unitário de transação 
    api_response = api_instance.notification(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RefundAPIV1Api->notification: %s\n" % e)
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

# **notifications**
> RefundProcess notifications(body)

Operação de registro em massa de uma transação

Método da API de Reporte de atualização em massa de APIs do Open Banking Brasil. O sistema utilizará essas informações para conciliar e contabilizar os custos das plataformas dos participantes. <br> Para a utilização deste método é necessário gerar um Token de Acesso na plataforma central do Diretório do Open Banking Brasil.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.RefundAPIV1Api()
body = [swagger_client.RefundNotification()] # list[RefundNotification] | 

try:
    # Operação de registro em massa de uma transação
    api_response = api_instance.notifications(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RefundAPIV1Api->notifications: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**list[RefundNotification]**](RefundNotification.md)|  | 

### Return type

[**RefundProcess**](RefundProcess.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

