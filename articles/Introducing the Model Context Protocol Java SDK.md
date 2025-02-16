from::rss
url::[Introducing the Model Context Protocol Java SDK](https://spring.io/blog/2025/02/14/mcp-java-sdk-released-2)
on:: 2025-02-16 08:02

MCP is an opensource model context protocol from Anthropic is a standardized way for LLMs to interact with data sources, tools, and AI agents. There's a growing system of pre-built integrations for this protocol.

Spring AI team collaborated with Anthropic on the project of supporting MCP in a Java API, starting last November, so Java is now added to the list of bindings for different languages at [Model Context Protocol](https://modelcontextprotocol.io). MCP Java SDK supports sync and async communication, various transport protocols (stdio, HTTP SSE streaming, Spring Web WebFlux/WebMVC integration).

Spring AI also provides various client and server starters. The article provides a sample configuration for a Client application to provide filesystem access as an MCP tool to Claude.

> Spring AI M6 also introduces the `@Tool` annotation, which simplifies the creation of MCP servers.

