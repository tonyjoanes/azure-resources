# Web API (ASP.NET Core) Best Practices

## Official Documentation

- [ASP.NET Core Web API Documentation](https://learn.microsoft.com/aspnet/core/web-api/)
- [RESTful web API design](https://learn.microsoft.com/azure/architecture/best-practices/api-design)
- [Microsoft REST API Guidelines](https://github.com/microsoft/api-guidelines)

## Key Best Practices

1. **Project Structure & Clean Code**
   - Use the [Clean Architecture](https://github.com/jasontaylordev/CleanArchitecture) template for scalable project organization.
   - Separate concerns: Controllers, Services, Repositories, DTOs.
   - Use Dependency Injection for all services.

2. **Error Handling & Validation**
   - Implement global exception handling middleware.
   - Use [FluentValidation](https://docs.fluentvalidation.net/en/latest/) for model validation.
   - Return appropriate HTTP status codes.

3. **Security**
   - Use HTTPS everywhere.
   - Implement authentication and authorization using ASP.NET Core Identity or JWT.
   - Validate and sanitize all inputs to prevent injection attacks.

4. **Versioning**
   - Use API versioning ([Microsoft.AspNetCore.Mvc.Versioning](https://github.com/dotnet/aspnet-api-versioning)).
   - Document all versions with Swagger.

5. **Documentation**
   - Use [Swashbuckle](https://github.com/domaindrivendev/Swashbuckle.AspNetCore) or [NSwag](https://github.com/RicoSuter/NSwag) for OpenAPI (Swagger) documentation.
   - Keep XML comments up to date.

6. **Logging & Monitoring**
   - Use built-in logging providers (Serilog, Seq, Application Insights).
   - Log requests/responses and errors.

7. **Testing**
   - Write unit and integration tests for controllers and services.
   - Use [xUnit](https://xunit.net/) or [NUnit](https://nunit.org/).

8. **Performance**
   - Use response caching and compression.
   - Profile APIs using BenchmarkDotNet or Application Insights.

## Templates & Examples

- [jasontaylordev/CleanArchitecture](https://github.com/jasontaylordev/CleanArchitecture)
- [dotnet-architecture/eShopOnWeb](https://github.com/dotnet-architecture/eShopOnWeb)
- [Microsoft Docs - Example Web API with Auth](https://learn.microsoft.com/samples/aspnet/aspnet-core/docs/)

---
