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

- [Azure-Samples/functions-dotnet-rest-api](https://github.com/Azure-Samples/functions-dotnet-rest-api)
- [brminnick/AzureFunctionsBestPractices](https://github.com/brminnick/AzureFunctionsBestPractices)
- [DavidParks8/Azure-Functions-Best-Practices](https://github.com/DavidParks8/Azure-Functions-Best-Practices)

---
