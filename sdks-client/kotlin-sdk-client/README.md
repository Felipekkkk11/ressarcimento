# io.swagger.client - Kotlin client library for Plataforma de Ressarcimento do Open Banking Brasil

## Requires

* Kotlin 1.4.30
* Gradle 5.3

## Build

First, create the gradle wrapper script:

```
gradle wrapper
```

Then, run:

```
./gradlew check assemble
```

This runs all tests and packages the library.

## Features/Implementation Notes

* Supports JSON inputs/outputs, File inputs, and Form inputs.
* Supports collection formats for query parameters: csv, tsv, ssv, pipes.
* Some Kotlin and Java types are fully qualified to avoid conflicts with types defined in Swagger definitions.
* Implementation of ApiClient is intended to reduce method counts, specifically to benefit Android targets.

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://ressarcimento.opbkdev.smartfylabs.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*RefundAPIV1Api* | [**findNotificationById**](docs/RefundAPIV1Api.md#findnotificationbyid) | **GET** /apis/v1/refund/notifications/{processId} | Operação de consulta de processos de transações
*RefundAPIV1Api* | [**healthcheck**](docs/RefundAPIV1Api.md#healthcheck) | **GET** /apis/v1/refund/notifications/healthcheck | Operação de consulta de monitoramento de processos de transações
*RefundAPIV1Api* | [**notification**](docs/RefundAPIV1Api.md#notification) | **POST** /apis/v1/refund/notifications/ | Operação de registro unitário de transação 
*RefundAPIV1Api* | [**notifications**](docs/RefundAPIV1Api.md#notifications) | **PATCH** /apis/v1/refund/notifications/ | Operação de registro em massa de uma transação

<a name="documentation-for-models"></a>
## Documentation for Models

 - [io.swagger.client.models.RefundNotification](docs/RefundNotification.md)
 - [io.swagger.client.models.RefundProcess](docs/RefundProcess.md)

<a name="documentation-for-authorization"></a>
## Documentation for Authorization

All endpoints do not require authorization.
