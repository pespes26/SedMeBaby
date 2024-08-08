# sed.py

A simple script to perform basic `sed`-like text manipulations on files or strings using Python.

## Description

`BasicSed.py` allows you to perform text substitutions, deletions, insertions, and other manipulations on text files or strings. The script supports multiple commands and provides feedback after each command is executed.

## Usage

### File Mode

To perform operations on a file, use the `-f` flag followed by the commands and the file name.

```bash
python BasicSed.py -f "command1;command2;..." filename
```

### Examples

- **Substitute (`s`)**: replace "brown" with "green" in example.txt:

  ```sh
  python sed.py -e "s/brown/green/" example.txt
  ```

- **Append (`a`)**: Append text after each line matched by a pattern:

  ```sh
  python sed.py -e "a/append/additional text/" sample.txt
  ```

- **Insert (`i`)**: Insert text before each line matched by a pattern on all lines:

  ```sh
  python BasicSedSed.py "i/sample/insert this text/" example.txt
  ```

- **Delete (`d`)**: Delete lines matching a pattern on lines:

  ```sh
  python sed.py -e "d/data/" example.txt
  ```

- **Print ('p')**: Print lines containing "All" in example.txt:

  ```sh
  python sed.py -e "p/pattern/" sample.txt
  ```

- **You can combine multiple commands using the -e option multiple times:**:

  ```sh
  python sed.py -e "s/old/new/" -e "d/remove/" sample.txt
  ```

- **Or using script file:**
  ```sh
  python sed.py -f script_file.sed sample.txt
  ```
  or
  ```sh
  python sed.py -e "command1;command2;..." filename.txt
  ```

## Options

- **-e**:Add the script of editing commands to the end of the script. This option can be used multiple times.
- **-f**:Add the editing commands in the file script_file to the end of the script. This option can be used multiple times.

### Output

For each command, the script provides feedback:

- If the pattern is found, it prints the relevant lines.
- If the pattern is not found, it prints a proper message.
- After all commands are executed, it prints the final content.

### Help

To display the help message with the available commands:

```bash
python sed.py --help
```

To activate the venv:

```bash
cd to the script path
venv\Scripts\activate
```

## Error Values

- 0: Successful completion.
- 1: No commands provided.
- 2: File not found.
- 3: Invalid command format.
- 4: Error processing file.
- 5: Error reading file.
- 6: Error writing file.
- 7: Unknown error.
