# learnix-os

A Rust operating system learning project.

## Development Setup with Skipper

This project uses [Skipper](https://github.com/stratoscale/skipper) for containerized development. All development tasks run inside a Docker container with the Rust toolchain pre-installed.

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Skipper](https://github.com/stratoscale/skipper) - Install with: `pip install strato-skipper`

### Quick Start

1. Build the development container:
   ```bash
   skipper build
   ```

2. Run common development tasks:
   ```bash
   # Build the project
   skipper make build
   
   # Run tests
   skipper make test
   
   # Run the application
   skipper make run
   
   # Format code
   skipper make fmt
   
   # Run clippy linter
   skipper make clippy
   
   # Open an interactive shell
   skipper make shell
   ```

### Configuration Files

- **`skipper.yaml`**: Skipper configuration defining the development environment
- **`Dockerfile.build`**: Docker image definition with Rust toolchain and development tools

### Environment Variables

The following environment variables are set in the container:
- `CARGO_HOME=/workspace/.cargo` - Cargo cache location
- `RUST_BACKTRACE=1` - Enable Rust backtraces for debugging