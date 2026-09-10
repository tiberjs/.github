# TiberJS

TiberJS is a collection of execution-first building blocks for Node.js and TypeScript. 

## Repositories

| Repository                                                    | Responsibility                                                                                                                                                                                                                                                          |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`tiberjs/runner`](https://github.com/tiberjs/runner)         | Independent execution runtime with immutable context, structured concurrency, scoped dependency injection, resource ownership, lifecycle events, cancellation, deadlines, and tracing. |
| [`tiberjs/server`](https://github.com/tiberjs/server)         | HTTP application framework, routing, middleware, validation, request and response handling, Node.js integration, HTTP feature packages, and route-aware tooling.                                                                                                        |
| [`tiberjs/transports`](https://github.com/tiberjs/transports) | WebSocket, microservice, gRPC, scheduling, Redis, Kafka, and RabbitMQ packages built on the runner execution model.                                                                                                                                                     |

The dependency direction is intentional:

```text
server ──────> runner
transports ──> runner
```

Runner has no dependency on either sibling repository, and server and transports remain independently releasable.

## Start here

Choose the repository that owns the problem you are solving:

- Use [`@tiberjs/runner`](https://github.com/tiberjs/runner) when you need the execution runtime without an application or protocol framework.
- Use [`@tiberjs/server`](https://github.com/tiberjs/server) for HTTP applications and HTTP-specific features.
- Use [`tiberjs/transports`](https://github.com/tiberjs/transports) for WebSocket, message, RPC, scheduling, or broker integrations.
