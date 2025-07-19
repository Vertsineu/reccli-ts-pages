# API Reference

This page provides detailed documentation for the RecCLI TypeScript API.

## RecCLI Class

The main class for creating CLI applications.

### Constructor

```typescript
new RecCLI(options?: RecCLIOptions): RecCLI
```

**Parameters**

- `options` (optional): Configuration options for the CLI

**Returns**

- A new `RecCLI` instance

### Methods

#### name()

Sets the name of the CLI application.

```typescript
name(name: string): RecCLI
```

#### version()

Sets the version of the CLI application.

```typescript
version(version: string): RecCLI
```

#### description()

Sets the description of the CLI application.

```typescript
description(desc: string): RecCLI
```

#### command()

Creates a new command.

```typescript
command(name: string, description?: string): Command
```

#### option()

Adds a global option to the CLI.

```typescript
option(flags: string, description?: string, defaultValue?: any): RecCLI
```

#### parse()

Parses the command line arguments and executes the matching command.

```typescript
parse(argv?: string[]): void
```

## Command Class

Represents a command in the CLI application.

### Methods

#### description()

Sets the description of the command.

```typescript
description(desc: string): Command
```

#### option()

Adds an option to the command.

```typescript
option(flags: string, description?: string, defaultValue?: any): Command
```

#### action()

Sets the action function for the command.

```typescript
action(fn: (...args: any[]) => void | Promise<void>): Command
```

## Option Interface

```typescript
interface Option {
  flags: string;
  description: string;
  defaultValue?: any;
  required?: boolean;
}
```

## More Examples

```typescript
import { RecCLI } from 'reccli-ts';

const cli = new RecCLI()
  .name('example')
  .version('1.0.0')
  .description('An example CLI application');

cli.command('hello <name>')
  .description('Say hello to someone')
  .option('-t, --times <number>', 'Number of times to say hello', 1)
  .action((name, options) => {
    for (let i = 0; i < options.times; i++) {
      console.log(`Hello, ${name}!`);
    }
  });

cli.parse();
```
