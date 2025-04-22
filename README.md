# MCP Playwright Server

A custom Playwright MCP (Multi-Client Protocol) server implementation that enables distributed test execution and browser automation across multiple clients.

## Features

- Distributed test execution across multiple clients
- Browser automation using Playwright
- Custom tool implementations for various browser operations
- Request/Response handling for MCP protocol
- Support for multiple browser contexts and pages

## Project Structure

```
├── mcp-playwright/
│   ├── src/
│   │   ├── tools/            # Tool implementations
│   │   │   ├── api/          # API-related tools
│   │   │   ├── browser/      # Browser automation tools
│   │   │   └── codegen/      # Code generation tools
│   │   ├── index.ts          # Main entry point
│   │   ├── requestHandler.ts  # MCP request handling
│   │   ├── toolHandler.ts     # Tool management
│   │   └── types.ts          # Type definitions
│   └── __tests__/            # Test files
├── package.json
└── tsconfig.json
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/DreViz/Playwrite_MCP.git
cd Playwrite_MCP
```

2. Install dependencies:
```bash
npm install
```

## Usage

To start the MCP server:

```bash
npm run mcp
```

This will start the Playwright MCP server that can handle requests from multiple clients.

## Tools

The server implements various tools for browser automation:

- **Browser Tools**:
  - Navigation
  - Screenshots
  - Console logging
  - User agent management
  - Page interactions
  
- **API Tools**:
  - Request handling
  - Response processing

- **CodeGen Tools**:
  - Test recording
  - Code generation

## Development

### Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)

### Setup Development Environment

1. Install development dependencies:
```bash
npm install
```

2. Run tests:
```bash
npm test
```

## Docker Support

The project includes Docker support for containerized execution:

1. Build the image:
```bash
docker build -t mcp-playwright .
```

2. Run the container:
```bash
docker run -p 3000:3000 mcp-playwright
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.