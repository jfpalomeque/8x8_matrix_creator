# 8x8 Grid Drawer Web App

A simple browser-based tool for creating and exporting 8x8 binary patterns. Perfect for creating pixel art templates, for led matrices such as max7219.

![image](https://github.com/user-attachments/assets/ab3b4bb6-a1e4-445a-9d48-23fda0af9758)


## Features

- **Interactive 8x8 Grid**: Click circular cells to toggle between black (0) and red (1)
- **Real-time Output**: Instantly generates formatted binary code with visual representation
- **One-click Copy**: Copy generated code to clipboard with a single button
- **Zero Dependencies**: Pure HTML/CSS/JavaScript - no frameworks or backend required

## Import Feature

The web app  supports importing existing patterns. This allows you to:

1. Share patterns between different sessions
2. Modify existing patterns
3. Store and retrieve patterns from text files

### How to Use the Import Feature

1. **Prepare Your Pattern**: Ensure your pattern is in the correct format:
    ```python
    [
        0b00011000,  #    XX
        0b00100100,  #   X  X
        0b01000010,  #  X    X
        0b01000010,  #  X    X
        0b01000010,  #  X    X
        0b00100100,  #   X  X
        0b00011000,  #    XX
        0b00000000   #       
    ]
    ```

2. **Import the Pattern**:
    - Paste your pattern into the import textarea
    - Click the "Import Pattern" button
    - The grid will update to match your pattern

### Format Requirements

- Must contain exactly 8 lines starting with `0b`
- Each `0b` must be followed by exactly 8 binary digits (0 or 1)
- Comments (after `#`) and whitespace are ignored
- Example of valid input:
    ```text
    0b00011000
    0b00100100
    0b01000010
    # ... etc ...
    ```

### Error Handling

- If the format is invalid, you'll see an error message
- The grid will remain unchanged if the import fails
- Common errors to avoid:
    - Missing or extra rows
    - Incorrect number of binary digits
    - Missing `0b` prefix

### Use Cases

- **Collaboration**: Share patterns with others via text
- **Version Control**: Store patterns in text files with Git
- **Backup**: Save your work as text for later use
- **Template Modification**: Start with existing patterns and modify them

### Example Workflow

1. Create a pattern in the web app
2. Copy the output using "Copy Output"
3. Save the text to a file
4. Later, paste the text back into the import box
5. Click "Import Pattern" to restore your work
