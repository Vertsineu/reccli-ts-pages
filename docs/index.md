# RecCLI TypeScript

Welcome to the RecCLI TypeScript documentation!

## Overview

RecCLI TypeScript is a powerful TypeScript library for developing command-line interfaces and tools. This documentation will help you get started with RecCLI TypeScript, understand its features, and learn how to use it effectively in your projects.

## Features

- **Type-Safe CLI Development**: Build robust command-line applications with TypeScript's type safety
- **Interactive Commands**: Create interactive command-line experiences
- **Extensible Architecture**: Easily extend and customize for your specific needs
- **Modern API Design**: Clean, modern API that's easy to use and understand

## Quick Start

Check out the [Getting Started](getting-started.md) guide to begin using RecCLI TypeScript in your projects.

```typescript
import { RecCLI } from 'reccli-ts';

const cli = new RecCLI()
  .command('hello', 'Say hello')
  .action(() => {
    console.log('Hello, world!');
  });

cli.parse();
```

## Contributing

We welcome contributions! See our [Contributing Guide](contributing.md) for more details.
