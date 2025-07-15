# Azure Functions Best Practices

## Official Documentation

- [Azure Functions Best Practices](https://learn.microsoft.com/azure/azure-functions/functions-best-practices)
- [Serverless Design Patterns and Best Practices](https://learn.microsoft.com/azure/architecture/serverless/)
- [Azure Functions Security Best Practices](https://learn.microsoft.com/azure/azure-functions/security-concepts)

## Key Best Practices

1. **Project Structure**
   - Group related functions in the same Function App.
   - Use dependency injection for shared services (from .NET 5+ isolated worker).

2. **Error Handling & Resilience**
   - Use [retry policies](https://learn.microsoft.com/azure/azure-functions/functions-bindings-error-pages?tabs=csharp#retry-policies) where applicable.
   - Log all exceptions with Application Insights.

3. **Configuration & Secrets**
   - Store settings in Azure App Configuration or Key Vault, not in code.
   - Use [Azure Managed Identities](https://learn.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview) for secure access.

4. **Performance & Scaling**
   - Avoid long-running operations; use Durable Functions for orchestrations.
   - Understand cold starts and optimize with premium plans if needed.

5. **Security**
   - Use function authorization levels (Function, Admin, Anonymous) appropriately.
   - Restrict network access with VNET integration or IP restrictions.

6. **Observability**
   - Enable Application Insights for monitoring and distributed tracing.
   - Use custom telemetry for business-critical events.

7. **Testing**
   - Write unit tests for your run methods and business logic.
   - Use integration testing for triggers and bindings.

## Templates & Examples

- [Azure-Samples/azure-functions-samples](https://github.com/Azure-Samples/azure-functions-samples)
- [Azure/azure-functions-dotnet-worker (samples folder)](https://github.com/Azure/azure-functions-dotnet-worker/tree/main/samples)
- [MicrosoftDocs/azure-docs - Azure Functions Samples](https://github.com/MicrosoftDocs/azure-docs/tree/main/articles/azure-functions/samples)

## Tutorials

- [Create a serverless API with Azure Functions](https://learn.microsoft.com/azure/azure-functions/functions-create-serverless-api)
- [Azure Functions HTTP trigger tutorial](https://learn.microsoft.com/azure/azure-functions/functions-bindings-http-webhook-trigger?tabs=csharp)

> **Note:** The previously listed `functions-dotnet-rest-api` sample does not exist (404). The above resources are maintained and provide up-to-date Azure Functions patterns for .NET.

---
