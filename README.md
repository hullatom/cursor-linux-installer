# Cursor Linux Installer

Cursor is an excellent AI-powered code editor, but it doesn't treat Linux as a first-class citizen. Unlike macOS and Windows, which have distribution-specific installers, Linux users are left with an AppImage that doesn't integrate well with the system. This means no `cursor` or `code` commands in your terminal, making it less convenient to use.

This repository aims to solve that problem by providing a set of shell scripts that will:

1. Download and install Cursor for you
2. Provide a `cursor` command that you can run from your shell
3. Allow you to easily update Cursor when new versions are released

## Installation

You can install the Cursor Linux Installer using either curl or wget. Choose the method you prefer:

### Using curl

```bash
curl -fsSL https://raw.githubusercontent.com/watzon/cursor-linux-installer/main/install.sh | bash
```

### Using wget

```bash
wget -qO- https://raw.githubusercontent.com/watzon/cursor-linux-installer/main/install.sh | bash
```

The installation script will:

1. Download the `cursor.sh` script and save it as `cursor` in `~/.local/bin/`
2. Make the script executable
3. Download and install the latest version of Cursor

## Uninstalling

To uninstall the Cursor Linux Installer, you can run the uninstall script:

```bash
curl -fsSL https://raw.githubusercontent.com/watzon/cursor-linux-installer/main/uninstall.sh | bash
```

or

```bash
wget -qO- https://raw.githubusercontent.com/watzon/cursor-linux-installer/main/uninstall.sh | bash
```

The uninstall script will:

1. Remove the `cursor` script from `~/.local/bin/`
2. Remove the Cursor AppImage
3. Ask if you want to remove the Cursor configuration files

## Usage

After installation, you can use the `cursor` command to launch Cursor or update it:

- To launch Cursor: `cursor`
- To update Cursor: `cursor --update`

## Note

If you encounter a warning that `~/.local/bin` is not in your PATH, you can add it by running:

```bash
export PATH="$HOME/bin:$PATH"
```

or add it to your shell profile (e.g., `.bashrc`, `.zshrc`, etc.):

```bash
echo "export PATH=\"\$HOME/bin:\$PATH\"" >> ~/.bashrc
source ~/.bashrc
```

## License

This software is released under the MIT License.

## Contributing

If you find a bug or have a feature request, please open an issue on GitHub.

If you want to contribute to the project, please fork the repository and submit a pull request.
