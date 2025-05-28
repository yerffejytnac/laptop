# macOS Development Environment Setup

A modern macOS development environment setup script based on [thoughtbot's laptop](https://github.com/thoughtbot/laptop) with customizations for contemporary development workflows.

## Features

- **Cross-platform compatibility**: Supports both Intel and Apple Silicon Macs
- **Modern toolchain**: Includes Bun, Deno, and other contemporary development tools
- **Mobile development**: Pre-configured for React Native and iOS development
- **Version management**: Uses asdf for managing multiple language versions
- **Shell enhancements**: Includes zsh with autosuggestions and Starship prompt

## What it installs

### Core Development Tools
- Git, Vim, tmux, and essential Unix utilities
- Homebrew package manager
- asdf version manager with Ruby and Node.js
- Zsh with autosuggestions and Starship prompt

### Languages & Runtimes
- Latest Ruby with Bundler configuration
- Latest Node.js with global npm packages
- Bun and Deno JavaScript runtimes

### Mobile Development
- Maestro for mobile app testing
- CocoaPods and Fastlane gems
- EAS CLI for Expo development
- iOS Simulator location utilities

### Applications
- OrbStack (Docker alternative)
- Eloston Chromium
- BetterDisplay

### CLI Tools
- GitHub CLI
- Supabase CLI
- Vercel CLI
- Biome (code formatter/linter)
- rclone (cloud storage sync)

## Installation

### Prerequisites
- macOS (Intel or Apple Silicon)
- Administrator access (for some installations)

### Quick Start

1. **Download and run the script:**
   ```bash
   curl --remote-name https://raw.githubusercontent.com/[your-username]/[your-repo]/main/mac
   sh mac 2>&1 | tee ~/laptop.log
   ```

2. **Or clone the repository:**
   ```bash
   git clone https://github.com/[your-username]/[your-repo].git
   cd [your-repo]
   sh mac 2>&1 | tee ~/laptop.log
   ```

3. **For local development (symlink method):**
   ```bash
   # Clone to your development directory
   git clone https://github.com/[your-username]/[your-repo].git ~/Development/laptop
   
   # Create a symlink in your home directory
   ln -sf ~/Development/laptop/mac ~/mac
   
   # Now you can run from anywhere
   sh ~/mac 2>&1 | tee ~/laptop.log
   ```

### What to expect

The script will:
1. Install Rosetta 2 (on Apple Silicon Macs)
2. Install and configure Homebrew
3. Install development tools and applications
4. Set up asdf version manager
5. Install latest Ruby and Node.js versions
6. Configure shell enhancements
7. Install mobile development tools

**Note**: The script may prompt for your password during installation of certain components. All output will be logged to `~/laptop.log` for troubleshooting.

## Customization

### Local customizations
Create a `~/.laptop.local` file to add your own customizations that will run after the main script:

```bash
#!/bin/sh

# Example local customizations
brew install --cask your-favorite-app
gem install your-favorite-gem
npm install -g your-favorite-package
```

### Modifying the script
Feel free to fork this repository and modify the `mac` script to suit your needs. The script is well-commented and organized into logical sections.

## Post-installation

After the script completes:

1. **Restart your terminal** or run `source ~/.zshrc` to apply shell changes
2. **Check the log file** at `~/laptop.log` for any issues or warnings
3. **Verify installations** by checking versions:
   ```bash
   ruby --version
   node --version
   brew --version
   ```

## Troubleshooting

### Common issues
- **Permission errors**: Ensure you have administrator access
- **Network issues**: Check your internet connection for downloads
- **Homebrew conflicts**: The script handles most common Homebrew issues automatically
- **Installation failures**: Check `~/laptop.log` for detailed error messages

### Getting help
- Check the [original thoughtbot/laptop issues](https://github.com/thoughtbot/laptop/issues) for common problems
- Review the `~/laptop.log` file for specific error messages
- Ensure your macOS is up to date

## Credits

This script is based on and inspired by [thoughtbot's laptop](https://github.com/thoughtbot/laptop), with modifications for modern development workflows and additional tools for mobile development.

## License

This project maintains the same license as the original thoughtbot/laptop repository.
