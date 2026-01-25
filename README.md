# File Management Toolkit

[![zread](https://img.shields.io/badge/Ask_Zread-_.svg?style=flat&color=00b0aa&labelColor=000000&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQuOTYxNTYgMS42MDAxSDIuMjQxNTZDMS44ODgxIDEuNjAwMSAxLjYwMTU2IDEuODg2NjQgMS42MDE1NiAyLjI0MDFWNC45NjAxQzEuNjAxNTYgNS4zMTM1NiAxLjg4ODEgNS42MDAxIDIuMjQxNTYgNS42MDAxSDQuOTYxNTZDNS4zMTUwMiA1LjYwMDEgNS42MDE1NiA1LjMxMzU2IDUuNjAxNTYgNC45NjAxVjIuMjQwMUM1LjYwMTU2IDEuODg2NjQgNS4zMTUwMiAxLjYwMDEgNC45NjE1NiAxLjYwMDFaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00Ljk2MTU2IDEwLjM5OTlIMi4yNDE1NkMxLjg4ODEgMTAuMzk5OSAxLjYwMTU2IDEwLjY4NjQgMS42MDE1NiAxMS4wMzk5VjEzLjc1OTlDMS42MDE1NiAxNC4xMTM0IDEuODg4MSAxNC4zOTk5IDIuMjQxNTYgMTQuMzk5OUg0Ljk2MTU2QzUuMzE1MDIgMTQuMzk5OSA1LjYwMTU2IDE0LjExMzQgNS42MDE1NiAxMy43NTk5VjExLjAzOTlDNS42MDE1NiAxMC42ODY0IDUuMzE1MDIgMTAuMzk5OSA0Ljk2MTU2IDEwLjM5OTlaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik0xMy43NTg0IDEuNjAwMUgxMS4wMzg0QzEwLjY4NSAxLjYwMDEgMTAuMzk4NCAxLjg4NjY0IDEwLjM5ODQgMi4yNDAxVjQuOTYwMUMxMC4zOTg0IDUuMzEzNTYgMTAuNjg1IDUuNjAwMSAxMS4wMzg0IDUuNjAwMUgxMy43NTg0QzE0LjExMTkgNS42MDAxIDE0LjM5ODQgNS4zMTM1NiAxNC4zOTg0IDQuOTYwMVYyLjI0MDFDMTQuMzk4NCAxLjg4NjY0IDE0LjExMTkgMS42MDAxIDEzLjc1ODQgMS42MDAxWiIgZmlsbD0iI2ZmZiIvPgo8cGF0aCBkPSJNNCAxMkwxMiA0TDQgMTJaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00IDEyTDEyIDQiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSIxLjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPgo8L3N2Zz4K&logoColor=ffffff)](https://zread.ai/YanivHaliwa/file-management-toolkit)
[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/YanivHaliwa/file-management-toolkit)

#version 14.6.25

A comprehensive collection of command-line tools for advanced file and data management operations. This toolkit provides powerful utilities for searching, comparing, compressing, and manipulating files with efficiency and precision.

## 🛠️ Tools Overview

### File Search & Discovery

#### `search` - Flexible file and folder searching with various options and filters
```bash
# Interactive file search (follows prompts for location, exact match, file type)
./search
```

#### `loc` - Fast file location using the system's `locate` command database
```bash
# Locate files in directory with search term
./loc /path/to/directory filename
```

#### `swd` - Advanced text search within files across directories with regex support
```bash
# Search for text pattern in directory
./swd /path/to/directory "search_term"

# Search with regex pattern
./swd -p /path/to/directory "regex_pattern"
```

#### `swf` - Pattern search within individual files with line number display
```bash
# Find specific pattern in a file
./swf script.py "import.*os"

# Search with regex pattern
./swf -p script.py "function.*main"
```

### File Comparison & Analysis

#### `comparef` - Intelligent file comparison between directories, identifying unique and common files while ignoring system directories (`.git`, `.trash`). Features colorful output for easy visualization
```bash
# Compare two directories
./comparef /path/to/dir1 /path/to/dir2
```

#### `list` - Generate comprehensive file listings from directories with recursive options and exclusion filters
```bash
# Create file listing (saves to file_list.txt)
./list /path/to/directory

# Create recursive file listing
./list /path/to/directory -r
```

### Data Processing & Cleanup

#### `dupl` - Remove duplicate lines from files while preserving original order
```bash
# Remove duplicates from file (output saved to uniq.txt)
./dupl input.txt
```

#### `reversefile` - Reverse Hebrew text content in files, creating new files with reversed content
```bash
# Reverse Hebrew text in file
./reversefile hebrew_text.txt
```

### Compression & Archives

#### `compr` - Universal compression/decompression tool supporting multiple formats: 7z, gzip, bzip2, xz, zstd, zip, rar, lz4, tar. Automatic format detection and optimal compression
```bash
# Compress files with 7zip
./compr -cz file1.txt file2.txt folder/

# Compress files with zpaq
./compr -cq file1.txt file2.txt folder/

# Extract/decompress any supported format (auto-detects)
./compr archive.7z
./compr compressed_file.gz
./compr archive.zip
```

### File Organization

#### `movef` - Advanced file organizer that moves all files from subdirectories to a destination directory with intelligent conflict resolution
```bash
# Move all files from subdirectories to destination directory
./movef /source/directory /destination/directory
```
**Features:**
- Moves files from all subdirectories to a single destination
- Automatically renames files with duplicate names using folder names
- Asks for confirmation before deleting empty subdirectories
- Preserves file integrity during the move operation

**Example:**
```bash
./movef /downloads/messy_folder /downloads/organized
# Moves all files from subdirectories to organized folder
```

### Specialized Tools

#### `readqr` - QR code reader that decodes QR codes from image files using barcode recognition API
```bash
# Read QR code from image
./readqr qrcode_image.png
```

#### `psearch` - APT package search utility with filtering for installed packages
```bash
# Search for packages (shows all matches)
./psearch package_name

# Search for packages with installation status
./psearch -i package_name
```

## 🚀 Key Features

- **Multi-format Support** - Handle various file types and compression formats
- **File Organization** - Advanced directory restructuring and file movement with conflict resolution
- **Regex Support** - Advanced pattern matching for text search operations
- **Colorized Output** - Enhanced visual feedback for better user experience
- **Recursive Operations** - Deep directory traversal capabilities
- **Smart Filtering** - Exclude system directories and unwanted files automatically
- **Cross-platform** - Works on Linux systems with standard utilities

## 📋 Requirements

### System Dependencies
```bash
# Core utilities (usually pre-installed)
locate
find
grep
tar
gzip

# For compression support
7zip
bzip2
xz-utils
zstd
unrar
lz4

# For QR code reading
curl (for API access)
```

### Installation of Dependencies
```bash
# Ubuntu/Debian
sudo apt update
sudo apt install locate findutils grep tar gzip p7zip-full bzip2 xz-utils zstd unrar lz4-tool curl

# Update locate database
sudo updatedb
```

## � Typical Workflows

### Workflow 1: Directory Organization & Cleanup
```bash
# 1. Compare two directories to see differences
./comparef /old/location /new/location

# 2. Organize scattered files from subdirectories
./movef /downloads/messy_folder /downloads/organized

# 3. Search for specific files in organized directory
./search # Follow prompts to search in /downloads/organized

# 4. Compress organized files for archival
./compr -cz /downloads/organized/
```

### Workflow 2: File Analysis & Deduplication
```bash
# 1. Generate file listing for analysis
./list /project/directory > file_inventory.txt

# 2. Search for duplicate content patterns
./swd /project/directory "duplicate_pattern"

# 3. Remove duplicate lines from data files
./dupl data_file.txt

# 4. Compress unique files
./compr -cz unique_files/
```

### Workflow 3: Package Management & System Search
```bash
# 1. Search for installed packages
./psearch -i software_name

# 2. Locate system files
./loc /usr/ config

# 3. Search within configuration files
./swf /etc/config.conf "setting_pattern"
```

## �🚀 Installation & Setup

### Clone the Repository
```bash
# Clone the repository
git clone https://github.com/YanivHaliwa/file-management-toolkit.git

# Navigate to the directory
cd file-management-toolkit

# Make all scripts executable
chmod +x *

# Optional: Add to your PATH for global access
sudo cp * /usr/local/bin/
# Or create symlinks
sudo ln -s $(pwd)/* /usr/local/bin/
```

### Verify Installation
```bash
# Test a few tools to ensure they work
./search
./loc --help
./readqr --help

# If added to PATH, you can use them globally
search
loc /home username
```

##  File Structure
```
file-management-toolkit/
├── README.md
├── .gitignore
├── comparef          # Directory comparison tool
├── compr             # Universal compression utility
├── dupl              # Duplicate line remover
├── list              # Directory listing generator
├── loc               # Fast file locator
├── psearch           # Package search utility
├── readqr            # QR code reader
├── reversefile       # Hebrew text reverser
├── search            # Advanced file search
├── swd               # Directory text search
└── swf               # File pattern search
```

## 🔒 Security Notes

- All tools operate locally and don't send data externally (except `readqr` which uses API)
- Scripts include input validation and error handling
- File operations preserve permissions when possible
- No destructive operations without explicit user confirmation

## 🐛 Troubleshooting

### Common Issues
1. **`locate` command not found**: Install `mlocate` package and run `sudo updatedb`
2. **Compression format not supported**: Install additional compression utilities
3. **Permission denied**: Ensure scripts have execute permissions (`chmod +x script_name`)
4. **QR code reading fails**: Check internet connection for API access

### Performance Tips
- Use `loc` for fast searches when filename is known
- Use `search` for complex file filtering
- Update locate database regularly: `sudo updatedb`
- For large directories, use exclusion filters to improve performance

## 🤝 Contributing

1. Test new tools thoroughly before adding
2. Follow existing naming conventions
3. Include usage examples in tool headers
4. Update this README when adding new tools

## 📄 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

Created by [Yaniv Haliwa](https://github.com/YanivHaliwa) for security testing and educational purposes.

---

**Note**: This toolkit is designed for system administrators, developers, and security professionals who need powerful file management capabilities from the command line.
