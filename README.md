# Playwright-MCP Container Demo

This is a demonstration on how to run Playwright-MCP in a container environment like Docker and Podman.

## How to run

1. Spin up the containers.
  ```bash
  podman compose up -d
  ```
2. Open browser: http://localhost:6274
3. Configure the inspector:
   1. Transport Type: Streamable HTTP
   2. URL: http://playwright:8931/mcp
4. Click on "Connect"
5. Now you should be connected an click "List Tools".

## Hints

- Playwright's default user agent will be blocked by many sites.
- User `podman compose logs -f` to check if everything is okay.
- See [demo.rest](./demo.rest) for a REST client friendly way to interact with the MCP server.

## Links

- [MCP Inspector](https://github.com/modelcontextprotocol/inspector)
- [Playwright MCP Container Image](https://hub.docker.com/r/mcp/playwright)
