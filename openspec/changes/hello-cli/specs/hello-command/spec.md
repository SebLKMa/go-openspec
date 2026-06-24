## ADDED Requirements

### Requirement: Greet by name
The program SHALL accept a single command-line argument and print "hello <arg>" to standard output, where `<arg>` is the provided argument.

#### Scenario: Greeting with a name
- **WHEN** the program is invoked with argument "world"
- **THEN** the program prints "hello world" to stdout

#### Scenario: Greeting with a different name
- **WHEN** the program is invoked with argument "Alice"
- **THEN** the program prints "hello Alice" to stdout

### Requirement: Usage error on missing argument
The program SHALL print a usage message to stderr and exit with a non-zero exit code when no argument is provided.

#### Scenario: No argument provided
- **WHEN** the program is invoked with no arguments
- **THEN** the program prints a usage message to stderr and exits with code 1
