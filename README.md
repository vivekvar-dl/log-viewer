# log-viewer

Real-time log viewer with filtering and syntax highlighting.

## Features

- 🎨 **Syntax highlighting** - Color-coded log levels, timestamps, IPs, HTTP codes
- 🔍 **Smart filtering** - Filter by level, regex patterns, or exclusions
- ⚡ **Real-time** - Tail multiple files simultaneously
- 🎯 **Simple** - No config files, just works

## Installation

```bash
curl -o ~/bin/log-viewer https://raw.githubusercontent.com/vivekvar-dl/log-viewer/main/log-viewer
chmod +x ~/bin/log-viewer
```

## Usage

```bash
# View log file with colors
log-viewer app.log --color

# Filter errors only
log-viewer app.log --level error --color

# Exclude health checks
log-viewer app.log --exclude "health-check" --color

# Multiple files
log-viewer app.log error.log --color

# Show last 50 lines
log-viewer app.log --lines 50 --color
```

## Syntax Highlighting

With `--color` flag, log-viewer automatically highlights:

- **ERROR/FATAL/CRITICAL** - Bold red
- **WARN/WARNING** - Bold yellow  
- **INFO** - Bold green
- **DEBUG/TRACE** - Gray
- **Timestamps** - Cyan (ISO8601, Apache, etc.)
- **IP addresses** - Blue
- **HTTP status codes** - Color by category (5xx red, 4xx yellow, 2xx green, 3xx cyan)
- **Quoted strings** - Magenta

## Options

```
-f, --filter REGEX   Filter lines matching regex
-e, --exclude REGEX  Exclude lines matching regex
-l, --level LEVEL    Filter by level (error|warn|info|debug)
-n, --lines N        Show last N lines (default: 10)
-c, --color          Enable syntax highlighting
-h, --help           Show help
```

## License

MIT
