# combine-files

Combines multiple files into one for ease of sharing/export.

## Installation

Requirements:

- Python
  - Libraries: argparse, fnmatch
- Git (to download this repository)

### Windows

1. Clone the repository

    ```bash
    git clone https://github.com/OK-Diamond/combine-files.git
    ```

2. Run:

    ```powershell
    notepad $PROFILE
    ```

    If prompted to create a file, click accept.

3. Paste this into the file:

   ```powershell
   function combine-files {
       & python "/full/path/to/combine_files.py" @args
   }
   ```

   (Replace `/full/path/to/combine_files.py` with the actual path)
4. Save the file (Ctrl+S) and close the window
5. Restart your terminal

### Linux

1. Clone the repository

   ```bash
   git clone https://github.com/OK-Diamond/combine-files.git
   ```

2. Make the script executable:

   ```bash
   chmod +x combine_files.py
   ```

3. Add an alias to your bash profile:

   ```bash
   echo 'alias combine-files="python /full/path/to/combine_files.py"' >> ~/.bashrc
   ```

   (Replace `/full/path/to/combine_files.py` with the actual path)

4. Reload your bash profile:

   ```bash
   source ~/.bashrc
   ```

### macOS

You're on your own, sorry! :P

## Usage

You should now be able to run the script through:

```bash
combine-files
```

For help with arguments:

```bash
combine-files -h
```

## Example

```bash
# Combine all Python files from a project into a single file
combine-files /path/to/project output.txt --include "*.py"

# Combine all code files except specific directories
combine-files /path/to/project output.txt --exclude-dirs "node_modules" "venv" "tmp"
```
