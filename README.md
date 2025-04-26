# MCP Client SSE

## Overview
The **MCP Client SSE** is a Spring Boot-based Java application that integrates with the Model Context Protocol (MCP). It provides a synchronous client implementation for interacting with MCP Servers and tools.

## Article
- [MCP Client Configuration](https://medium.com/@shaamamanoharan/configuring-mcp-client-sse-in-spring-boot-fb07371c35a7)

## Features
- Synchronous MCP client integration.
- Configurable tool callback provider.
- OpenAI API integration.
- Customizable application properties.

## Configuration
The application can be configured using the `application.properties` file located in `src/main/resources`. Below are the key configuration properties:

### OpenAI Configuration
```ini
spring.ai.openai.api-key=<OPEN_AI_API_KEY>
```

### MCP Client Configuration
```properties
spring.ai.mcp.client.enabled=true
spring.ai.mcp.client.name=my-mcp-client
spring.ai.mcp.client.version=1.0.0
spring.ai.mcp.client.request-timeout=30s
spring.ai.mcp.client.type=SYNC
spring.ai.mcp.client.sse.connections.server1.url=http://localhost:8082 # MCP SERVER
spring.ai.mcp.client.toolcallback.enabled=true
```

## How to Run
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd mcp-client
   ```

2. Build the project using Gradle:
   ```bash
   ./gradlew build
   ```

3. Run the application:
   ```bash
   ./gradlew bootRun
   ```

4. The application will start on the default port `8080`.

## Dependencies
- Spring Boot
- MCP Client Library
- OpenAI API

## References:

- [Spring AI Documentation](https://docs.spring.io/spring-ai/reference/index.html)
- [MCP Client Documentation](https://docs.spring.io/spring-ai/reference/api/mcp/mcp-client-boot-starter-docs.html)
- [Tool Calling Documentation](https://docs.spring.io/spring-ai/reference/api/tools.html)
