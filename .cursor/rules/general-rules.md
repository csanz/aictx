# Codebase Maintenance Rules

## General 

- Use appropriate development servers for the project type (e.g., http-server for static sites, webpack-dev-server for JS apps)
- Choose frameworks and libraries based on project requirements and team expertise
- Always confirm with the user before starting any servers or services
- Follow established patterns in the existing codebase
- Prioritize maintainability and readability over clever solutions

## Documentation
- Add clear, descriptive comments to all files explaining their purpose and key functionality
- Use JSDoc or similar documentation standards for functions and classes
- Document edge cases and complex logic with examples
- Create a CONTEXT.md at the root if it doesn't exist. 
- Maintain an up-to-date CONTEXT.md file at the project root that:
  - Describes the current state of the application
  - Explains what each component does
  - Documents how files relate to each other
  - Includes a directory structure overview

## README Documentation
- Ensure the README.md is comprehensive and well-structured:
  - Start with a clear, concise project description and purpose
  - Include visually appealing badges (build status, version, license)
  - Add installation instructions with prerequisites and environment setup
  - Provide quick start examples that work without modification
  - Document all features with examples and screenshots where appropriate
  - Include API/CLI reference with all commands, options, and parameters
  - Add troubleshooting section for common issues
  - Provide contribution guidelines and code of conduct
  - Keep the README updated with every significant change to the codebase
  - Use proper markdown formatting with headings, lists, code blocks, and tables

## Configuration Management
- Store all configuration values used across multiple files in config.json
  - Use consistent naming conventions (camelCase or snake_case)
  - Group related settings under namespaced objects
  - Include appropriate documentation for each setting
  - Mark deprecated settings with comments

## Code Context
- Always check the latest-context.txt file (if it exists) to understand the current codebase state
  - This file is automatically generated and provides a comprehensive view of the project
  - Located at ./context/latest-context.txt
  - Use this as your primary reference before making changes
- When generating context files with `cx ./` command:
  - Exclude binary files, compilation artifacts, and build outputs
  - Focus on source code files that provide meaningful context
  - Use appropriate flags (e.g., `-i` or `--ignore`) to exclude irrelevant directories or file types

## Code Quality
- Follow the established code style of the project
- Write self-documenting code with clear variable and function names
- Keep functions small and focused on a single responsibility
- Add unit tests for new functionality

## Version Control
- Write meaningful commit messages that explain why changes were made
- Update version numbers according to semantic versioning principles
- Keep the changelog updated with all significant changes 
- Never commit binary files, compilation artifacts, or build outputs (e.g., *.o, *.exe, *.dll, *.so)
- Use .gitignore to properly exclude build directories, dependency folders, and temporary files
- Verify what files are being staged before committing to avoid accidental inclusion of binary artifacts 