# Perplexity API OpenAPI Specification

This repository contains an OpenAPI 3.0.3 specification for the [Perplexity API](https://docs.perplexity.ai/api-reference/chat-completions).

## Overview

The Perplexity API allows developers to integrate powerful AI models with search capabilities. The API is OpenAI-compatible for easy integration with existing applications.

## Specification

The OpenAPI specification (`perplexity-openapi.yaml`) includes:

- Authentication method (Bearer token)
- Available endpoints (`/chat/completions`)
- Request and response schemas
- Available models
- Parameters for controlling model behavior
- Structured output formats (JSON Schema and Regex)

## Available Models

- `sonar-deep-research`: Performs exhaustive research across many sources
- `sonar-reasoning-pro`: Premier reasoning offering powered by DeepSeek R1 with Chain of Thought
- `sonar-pro`: Premier search offering with search grounding
- `sonar`: Lightweight offering with search grounding
- `r1-1776`: DeepSeek R1 model post-trained for uncensored, unbiased information

## Usage

You can use this OpenAPI specification to:

1. Generate client libraries in various programming languages
2. Set up API documentation
3. Test API endpoints with tools like Postman or Swagger UI
4. Validate API requests and responses

## Example Request

```bash
curl --location 'https://api.perplexity.ai/chat/completions' \
--header 'accept: application/json' \
--header 'content-type: application/json' \
--header 'Authorization: Bearer {API_KEY}' \
--data '{
  "model": "sonar-pro",
  "messages": [
    {
      "role": "system",
      "content": "Be precise and concise."
    },
    {
      "role": "user",
      "content": "How many stars are there in our galaxy?"
    }
  ]
}'
```

## Rate Limits

Rate limits vary by model and usage tier. Please refer to the [official documentation](https://docs.perplexity.ai/api-reference/chat-completions) for the most up-to-date information.

## Resources

- [Perplexity API Documentation](https://docs.perplexity.ai/api-reference/chat-completions)
- [Getting Started Guide](https://docs.perplexity.ai/guides/getting-started)
- [Structured Outputs Guide](https://docs.perplexity.ai/guides/structured-outputs)
