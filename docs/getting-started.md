# Getting Started

This guide will help you get started with RecCLI TypeScript.

## Installation

Install RecCLI TypeScript using npm:

```bash
npm install reccli-ts
```

Or using yarn:

```bash
yarn add reccli-ts
```

## Basic Usage

Here's a simple example to create a CLI application:

```typescript
import { RecCLI } from 'reccli-ts';

// Create a new CLI instance
const cli = new RecCLI()
  .name('my-cli')
  .version('1.0.0')
  .description('My awesome CLI tool');

// Add a command
cli.command('greet <name>')
  .description('Greet someone')
  .option('-l, --loud', 'Greet loudly')
  .action((name, options) => {
    const greeting = `Hello, ${name}!`;
    if (options.loud) {
      console.log(greeting.toUpperCase());
    } else {
      console.log(greeting);
    }
  });

// Parse arguments and execute
cli.parse(process.argv);
```

## Next Steps

- Explore the [User Guide](user-guide/index.md) for more detailed information
- Check out the [API Reference](api-reference.md) for a complete list of available methods and options
