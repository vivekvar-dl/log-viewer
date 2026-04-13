# log-viewer

Real-time log viewer with filtering and highlighting.

## Installation

```bash
curl -o ~/bin/log-viewer https://raw.githubusercontent.com/vivekvar-dl/log-viewer/main/log-viewer
chmod +x ~/bin/log-viewer
```

## Usage

```bash
# View log file
log-viewer app.log

# Filter errors
log-viewer app.log --level error

# Exclude health checks
log-viewer app.log --exclude "health"
```

## License

MIT
