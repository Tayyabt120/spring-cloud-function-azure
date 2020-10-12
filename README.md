# spring-cloud-function-azure
spring-cloud-function-azure


# Example "Hello, world" Spring Boot application that runs on Azure Functions

This is a sample application to showcase the use of Spring Cloud Function on top of Azure Functions.

### Installation

- Clone the project
- Build the project: `./mvnw clean package`

### Quickstart

Once the application is built, you can run it locally using the Azure Function Maven plug-in:

`./mvnw azure-functions:run`

And you can test it using a cURL command:

`curl http://localhost:7071/api/currency-converter -d "{\"amount\": 200.0,\"from\": \"USD\",\"to\": \"INR\",\"convertedValue\": 14669.640000000001}"`

## Deploying to Azure Functions

Deploy the application on Azure Functions with the Azure Function Maven plug-in:

`./mvnw azure-functions:deploy`

You can then test the running application, by running a POST request:

```
curl https://<YOUR_SPRING_FUNCTION_NAME>.azurewebsites.net/api/currency-converter -d "{\"amount\": 200.0,\"from\": \"USD\",\"to\": \"INR\",\"convertedValue\": 14669.640000000001}"
```

Replace the `<YOUR_SPRING_FUNCTION_NAME>` part by the name of your Spring Function.
