# Awesome OpenCode - Agent Guidelines

This document provides comprehensive information about the tools and capabilities available when using OpenCode agents with custom modes.

## Available Tools

### File System Tools

#### 1. **Read**

- **Purpose**: Read files from the local filesystem
- **Key Features**:
  - Supports reading any file with absolute paths
  - Reads up to 2000 lines by default (configurable with offset/limit)
  - Supports image files (PNG, JPG, etc.) with visual display
  - Returns content with line numbers (cat -n format)
  - Batch reading capability for multiple files

#### 2. **Write**

- **Purpose**: Create new files or completely replace existing file contents
- **Key Features**:
  - Creates parent directories automatically
  - Overwrites entire file content
  - Best for creating new files or complete replacements

#### 3. **Edit**

- **Purpose**: Make precise edits to existing files
- **Key Features**:
  - Line-based editing with before/after patterns
  - Preserves file structure and formatting
  - Ideal for targeted modifications

#### 4. **MultiEdit**

- **Purpose**: Apply multiple edits to files in a single operation
- **Key Features**:
  - Batch editing across multiple files
  - Atomic operations (all succeed or all fail)
  - Efficient for large-scale refactoring

#### 5. **LS (List)**

- **Purpose**: List directory contents
- **Key Features**:
  - Shows files and subdirectories
  - Supports glob pattern filtering
  - Returns structured directory information

### Search Tools

#### 6. **Grep**

- **Purpose**: Search file contents using regular expressions
- **Key Features**:
  - Full regex support
  - File pattern filtering (e.g., "_.js", "_.{ts,tsx}")
  - Returns matching file paths sorted by modification time
  - Optimized for large codebases

#### 7. **Glob**

- **Purpose**: Find files by name patterns
- **Key Features**:
  - Supports glob patterns like "**/\*.js" or "src/**/\*.ts"
  - Fast pattern matching
  - Returns paths sorted by modification time

### Command Execution

#### 8. **Bash**

- **Purpose**: Execute shell commands
- **Key Features**:
  - Persistent shell session
  - Configurable timeout (up to 10 minutes)
  - Proper handling of spaces in paths
  - Git integration with commit guidelines
  - Parallel command execution support
- **Important Notes**:
  - Avoid using `find` and `grep` commands (use Grep/Glob tools instead)
  - Use `rg` (ripgrep) instead of grep when needed
  - Maintain working directory with absolute paths

### Task Management

#### 9. **TodoWrite**

- **Purpose**: Create and manage task lists
- **When to Use**:
  - Complex multi-step tasks (3+ steps)
  - User provides multiple tasks
  - Tracking progress on non-trivial work
- **Task States**:
  - `pending`: Not yet started
  - `in_progress`: Currently working (limit to one at a time)
  - `completed`: Finished successfully
  - `cancelled`: No longer needed

#### 10. **TodoRead**

- **Purpose**: Read current task list
- **Use Case**: Check task status and remaining work

### AI-Powered Tools

#### 11. **Task (Agent)**

- **Purpose**: Launch autonomous agents for complex searches or tasks
- **When to Use**:
  - Open-ended searches requiring multiple rounds
  - Complex analysis tasks
  - When you need parallel exploration
- **Capabilities**: Access to all other tools

### Web Tools

#### 12. **WebFetch**

- **Purpose**: Fetch and analyze web content
- **Features**:
  - Converts HTML to markdown
  - Supports multiple formats (text, markdown, HTML)
  - 15-minute cache for efficiency
  - Configurable timeout

#### 13. **WebSearch**

- **Purpose**: Search the web for information
- **Use Case**: Finding documentation, solutions, or external resources

### Language Server Protocol (LSP) Tools

#### 14. **LSP-Diagnostics**

- **Purpose**: Get code diagnostics and errors
- **Features**: Type errors, linting issues, compilation problems

#### 15. **LSP-Hover**

- **Purpose**: Get type information and documentation
- **Features**: Variable types, function signatures, inline docs

## Best Practices

### 1. Tool Selection

- Use specialized tools over Bash commands when available
- Batch operations when possible (e.g., reading multiple files)
- Prefer Task tool for complex, open-ended searches

### 2. File Operations

- Always use absolute paths
- Check parent directories exist before creating files
- Use Edit for modifications, Write for new files
- Quote paths with spaces in Bash commands

### 3. Search Strategy

- Start broad with Glob/Grep, then narrow down
- Use Task tool when initial search scope is unclear
- Combine multiple search patterns for comprehensive results

### 4. Task Management

- Use TodoWrite for any task with 3+ steps
- Mark tasks as in_progress when starting
- Complete tasks immediately when done
- Only one in_progress task at a time

### 5. Git Operations

- Always check status, diff, and log before committing
- Follow repository's commit message style
- Include co-author attribution for OpenCode
- Never commit without explicit user request

## Custom Mode Integration

When creating custom modes for awesome-opencode:

### 1. Tool Availability

- All tools listed above are available in custom modes
- Tools can be combined for complex workflows
- Consider tool limitations when designing modes

### 2. Mode Design Guidelines

- Clearly specify which tools the mode will use
- Document any special tool configurations
- Provide examples of tool usage in context
- Consider performance implications of tool choices

### 3. Common Patterns

```yaml
# Example: Code Review Mode
tools_used:
  - Grep: Find code patterns
  - Read: Examine specific files
  - LSP-Diagnostics: Check for errors
  - TodoWrite: Track review items

# Example: Refactoring Mode
tools_used:
  - Glob: Find target files
  - MultiEdit: Batch modifications
  - Bash: Run tests
  - Task: Complex analysis

# Example: Documentation Mode
tools_used:
  - Glob: Find relevant files
  - Read: Extract code examples
  - Write: Create documentation
  - WebSearch: Find best practices
```

### 4. Performance Considerations

- Batch tool calls when possible
- Use Task for exploratory work
- Cache results with WebFetch
- Limit file reads to necessary content

## Security Notes

- Never expose or log secrets/keys
- Refuse requests for malicious code
- Validate file paths before operations
- Follow security best practices in all operations

## Environment Information

OpenCode agents have access to:

- Full filesystem (with appropriate permissions)
- Network access for web tools
- Git repositories and version control
- Language servers for code intelligence
- Persistent shell sessions

Remember: The key to effective custom modes is understanding tool capabilities and combining them creatively to solve specific use cases.
