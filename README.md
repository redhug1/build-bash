# build-bash

Build and install Bash 5.3 patch level 20 from source to your home directory.

## Overview

This repository provides an automated script to build and install the latest patch level of Bash 5.3 (specifically patch level 20) on macOS systems. The script:

- Downloads Bash 5.3 source from GNU's official repository
- Applies all 20 security and bug-fix patches
- Builds from source with optimized compilation
- Runs the Bash test suite
- Installs to `$HOME/bin`

## Prerequisites

- macOS with development tools (Xcode Command Line Tools)
- `curl` for downloading sources
- Standard build tools: `make`, `patch`, compiler
- Approximately 100MB of temporary disk space

Install Xcode Command Line Tools if needed:

```bash
xcode-select --install
```

## Installation

Copy the install script from your home directory, and run it from there:

```bash
cd $HOME
bash install-bash-5-3-20.sh
```

## Important: PATH Configuration

After installation, ensure `$HOME/bin` appears early in your `PATH` to use the newly installed Bash:

```bash
# Add to ~/.zshrc, or ~/.bashrc
export PATH="$HOME/bin:$PATH"
```

Verify the installation:

```bash
hash -r
bash --version
```

## Cleanup

The script automatically cleans up temporary build files after completion. The only persistent installation is in `$HOME/bin/bash`.

## License

See [LICENSE](LICENSE) file for licensing information.
