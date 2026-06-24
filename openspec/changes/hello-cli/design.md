## Context

This is a greenfield project with no existing code. We need to add a simple CLI program that prints a greeting using a command-line argument.

## Goals / Non-Goals

**Goals:**
- Create a minimal CLI that takes a name argument and prints "hello <name>"
- Keep it simple — one file, no dependencies beyond the standard library

**Non-Goals:**
- Multiple arguments or flags
- Interactive input
- Internationalization

## Decisions

**Language: Go**
The project directory is under a Go workspace path (`go/github.com/...`). Go produces a single static binary with no runtime dependencies, ideal for a CLI tool. Alternative considered: a shell script — rejected because Go gives us type safety and a proper build artifact.

**Argument handling: `os.Args` directly**
For a single required argument, `os.Args` is sufficient. No need for a flag-parsing library. Alternative considered: `flag` package — rejected as unnecessary for a positional argument.

## Risks / Trade-offs

- [Minimal error handling] → Print a usage message and exit with code 1 if no argument is provided.
