<div style="text-align: center;">
    <img src="assets/logo.png" width=150 />
</div>

# Sentio Custom Integration Template

This is an example template for creating custom integrations with Sentio. It demonstrates how to structure your integration code and provides a TypeScript-based foundation.

## Features

- TypeScript support with modern configuration
- Docker support for containerized applications
- Development and production build scripts
- Git configuration with appropriate ignores
- Ready-to-use project structure

## Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager

## Project Structure

```
sentio-custom-integration-template/
├── src/                    # Source code directory
│   └── index.ts           # Main entry point
├── dist/                   # Compiled JavaScript output
├── Dockerfile             # Container configuration
├── package.json           # Project dependencies and scripts
├── tsconfig.json          # TypeScript configuration
└── .gitignore            # Git ignore rules
```

## Getting Started

1. Use this template as a starting point for your integration:

   ```bash
   git clone <your-repo-url>
   cd your-integration-name
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start development:

   ```bash
   npm run dev
   ```

4. Build for production:

   ```bash
   npm run build
   ```

5. Run the production build:
   ```bash
   npm start
   ```

## Docker Support

This template includes a basic Dockerfile to help you containerize your integration. You can modify it according to your specific needs:

```dockerfile
FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

CMD ["npm", "start"]
```

## Available Scripts

- `npm run dev`: Run the application in development mode using ts-node
- `npm run build`: Compile TypeScript to JavaScript
- `npm start`: Run the compiled JavaScript code
- `npm test`: Run tests (to be implemented)

## Development

The template uses TypeScript with the following features:

- Modern ES2020 target
- Strict type checking
- CommonJS modules
- Source maps for debugging

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License - see the LICENSE file for details.

## Support

For support, please open an issue in the repository or contact the Sentio team.
