# User Guide

Welcome to the RecCLI TypeScript User Guide! This section provides detailed information about using RecCLI TypeScript in your projects.

## Table of Contents

- [Installation](installation.md) - How to install RecCLI TypeScript
- Commands - How to define and use commands
- Options - Working with command options
- Arguments - Handling command arguments
- Interactive Prompts - Creating interactive CLI experiences
- Error Handling - Best practices for handling errors
- Testing - How to test your CLI applications

## Core Concepts

RecCLI TypeScript is built around a few core concepts:

### CLI Instance

The main entry point for your application is the `RecCLI` class. This class provides methods for configuring your CLI application, adding commands, and parsing arguments.

### Commands

Commands represent the different actions that your CLI application can perform. Each command can have its own options, arguments, and action handler.

### Options

Options are flags that modify the behavior of a command. They can be boolean flags or take values.

### Arguments

Arguments are positional parameters passed to a command. They can be required or optional.

### Actions

Actions are functions that are executed when a command is invoked. They receive the parsed arguments and options as parameters.
