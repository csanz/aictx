# AICTX (AI Context Generator)

![AICTX Brain](static/brain.jpg)

A command-line tool that generates context files from your codebase for use with AI tools like Cursor, ChatGPT, or Claude.

## Features

- 📁 Scans directories for JavaScript and JSON files
- 🌳 Includes full directory structure
- 📝 Creates comprehensive context files
- 🗜️ Optional text compression to reduce context size
- 🔄 Automatic sequence numbering for multiple scans
- 📋 Maintains code readability for AI tools
- ✨ Automatic .gitignore management

## Installation

```bash
npm install -g aictx
```

## Usage

```bash
cx <directory> [options]
```

## Options

- `-h, --help`: Show help
- `--no-compress`: Skip compression of the output file

## Example

```bash
cx ./src
```

This will:
1. Scan the `./src` directory for JS and JSON files
2. Create a `context/code` directory (if it doesn't exist)
3. Generate a context file with the directory structure and file contents
4. Create both regular and compressed versions (unless --no-compress is used)
5. Automatically add `context/` to .gitignore

## Output

The tool generates two files (when compression is enabled):
- `context/code/<directory>-context-<n>.txt`: Full context file
- `context/code/<directory>-context-<n>.txt.min`: Compressed version

The sequence number `<n>` automatically increments for each new scan.

## Why Use AICTX?

- **AI Context**: Provides AI tools with complete codebase understanding
- **Time Saving**: Quickly generates comprehensive context files
- **Space Efficient**: Optimized compression while maintaining readability
- **Version Control Friendly**: Automatic .gitignore management
- **Sequential Tracking**: Maintains history of context generations

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT

