---
navigation_title: EDOT SDKs
description: An overview of the features available in the Elastic Distribution of OpenTelemetry (EDOT) SDKs for various languages.
applies_to:
  stack:
  serverless:
    observability:
products:
  - id: cloud-serverless
  - id: observability
  - id: edot-sdk
---

# EDOT SDKs 

The {{edot}} (EDOT) SDKs are production-ready, customized distributions of [OpenTelemetry](https://opentelemetry.io/) language SDKs, specifically optimized for seamless integration with Elastic Observability. EDOT SDKs provide a comprehensive observability solution that automatically captures distributed traces, metrics, and logs from your applications with minimal configuration.

While maintaining full compatibility with the OpenTelemetry specification, EDOT SDKs provide improvements and bug fixes from Elastic before they become available in upstream OpenTelemetry repositories.

## Supported languages

EDOT SDKs are available for the following programming languages and platforms:

* [.NET](/reference/edot-sdks/dotnet/index.md)
* [Java](/reference/edot-sdks/java/index.md)
* [Node.js](/reference/edot-sdks/nodejs/index.md)
* [PHP](/reference/edot-sdks/php/index.md)
* [Python](/reference/edot-sdks/python/index.md)
* [Android](/reference/edot-sdks/android/index.md)
* [iOS](/reference/edot-sdks/ios/index.md)

## Feature overview

This table provides an overview of the features available in the {{edot}} (EDOT) SDKs across different programming languages.

% start:edot-features

| Feature | .NET | Java | Node.js | PHP | Python | Android | iOS |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **[Distributed Tracing](https://opentelemetry.io/docs/concepts/signals/traces/)** | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | 
| [Service Map](docs-content://solutions/observability/apm/service-map.md) | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ v1.0+ | 
| [Zero-code instrumentation](https://opentelemetry.io/docs/concepts/instrumentation/zero-code/) | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ❌  | ❌  | 
| [Head-based Sampling](https://opentelemetry.io/docs/concepts/sampling/#head-sampling) | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.1+ | ✅ v1.0+ | 
| [Baggage](https://opentelemetry.io/docs/concepts/signals/baggage/) | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ❌  | ✅ v1.0+ | 
| [Inferred Spans](./java/features.md#inferred-spans) | ❌  | ✅ 1.0+ | ❌  | 𝐓 1.0+ | ❌  | ❌  | ❌  | 
| **[Logs Collection](https://opentelemetry.io/docs/specs/otel/logs/#opentelemetry-solution)** | ✅ 1.0+ | ✅ 1.0+ | 𝐓 1.0+ | ✅ 1.0+ | 𝐓 1.0+ | ✅ 1.0+ | ✅ v1.0+ | 
| [Logs Correlation](https://opentelemetry.io/docs/specs/otel/logs/#log-correlation) | ✅ 1.0+ | ✅ 1.0+ | 𝐓 1.0+ | ✅ 1.0+ | 𝐓 1.0+ | ✅ 1.0+ | ✅ v1.0+ | 
| **[Metrics Collection](https://opentelemetry.io/docs/concepts/signals/metrics/)** | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | 𝐓 v0.7+ | 
| Custom Metrics | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | 𝐓 v0.7+ | 
| Agent Health Monitoring | ❌  | ❌  | ❌  | ❌  | ❌  | ❌  | ❌  | 
| [Runtime Metrics](https://opentelemetry.io/docs/specs/semconv/runtime/) | ✅ 1.0+ | ✅ 1.0+ | 𝐓 1.0+ | ❌  | ❌  | ❌  | ❌  | 
| **Capturing Errors / Exceptions** | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ 1.0+ | ✅ v1.0+ | 
| Crash Reporting | ➖  | ➖  | ➖  | ➖  | ➖  | ❌  | ✅ v1.0+ | 
| **Central Configuration** | ❌  | 𝐓 1.5.0+ | 𝐓 1.2.0+ | 𝐓 1.1.1+ | 𝐓 1.4.0+ | 𝐓 1.2.0+  | ❌  | 
| **[Profiling Integration](./java/features.md#elastic-universal-profiling-integration)** | ❌  | 𝐓 1.0+ | ❌  | ❌  | ❌  | ❌  | ❌  | 

**Legend:**

* ✅ Generally available
* 𝐓 In technical preview
* ➖ Not applicable
* ❌ Not available
% end:edot-features

## Support for EDOT SDKs

Elastic provides technical support for EDOT Language SDKs according to Elastic's [Support Policy](https://www.elastic.co/support_policy). EDOT SDKs are meant to be used in combination with the [EDOT Collector](/reference/edot-collector/index.md) or the [{{motlp}}](/reference/motlp.md) to ingest data into Elastic solutions from the EDOT SDKs. Other ingestion paths are not officially supported by Elastic.

:::{warning}
Avoid using EDOT SDKs alongside any other APM agent, including Elastic APM agents. Running multiple agents in the same application process may lead to conflicting instrumentation, duplicate telemetry, or other unexpected behavior.
:::

## License

EDOT SDKs are licensed under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).
