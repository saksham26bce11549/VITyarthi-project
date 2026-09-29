# VITyarthi-project
# Simple Text Editor

A simple text editor application built using **Python** and **Tkinter**.  
It provides a basic graphical user interface (GUI) that allows users to create, open, edit, and save text files.

## Features

- Create a new text document
- Open existing `.txt` files
- Edit text using a text area
- Save files as `.txt`
- Simple File menu
- Exit the application
- Displays a confirmation message after saving

## Technologies Used

- **Python 3**
- **Tkinter** – Used to create the graphical user interface
- **tkinter.filedialog** – Used for opening and saving files
- **tkinter.messagebox** – Used to display messages to the user

## Requirements

Python 3 must be installed on your computer.

Tkinter is usually included with Python. To check if it is installed, run:

```bash
python3 -m tkinter
```

If a Tkinter window appears, it is installed correctly.

## How to Run

1. Save the Python code in a file, for example:

```text
text_editor.py
```

2. Open Terminal or Command Prompt.

3. Navigate to the folder containing the file.

4. Run:

```bash
python3 text_editor.py
```

The **Simple Text Editor** window will open.

## How It Works

### 1. Main Window

The program creates the main application window using:

```python
root = tk.Tk()
```

The window is given the title **Simple Text Editor** and a size of **800 × 600**.

### 2. Text Area

A Tkinter `Text` widget is used as the main editing area.

```python
text = tk.Text(
    root,
    wrap=tk.WORD,
    font=("Helvetica", 18)
)
```

The text automatically wraps to the next line when it reaches the edge of the window.

### 3. New File

The `new_file()` function clears the text area:

```python
def new_file():
    text.delete(1.0, tk.END)
```

This allows the user to start writing a new document.

### 4. Open File

The `open_file()` function displays a file-selection dialog.

The user can select a `.txt` file, and its contents are loaded into the text area.

```python
file_path = filedialog.askopenfilename(...)
```

The existing text is cleared before the selected file's contents are inserted.

### 5. Save File

The `save_file()` function opens a save dialog and writes the text area contents into the selected file.

```python
file.write(text.get(1.0, tk.END))
```

After successfully saving, a message box displays:

```text
File saved successfully
```

### 6. Menu Bar

The application contains a **File** menu with the following options:

- **New** – Clears the current text
- **Open** – Opens an existing text file
- **Save** – Saves the current text
- **Exit** – Closes the application

## Project Structure

```text
Simple-Text-Editor/
│
├── text_editor.py
└── README.md
```

## Limitations

This is a basic text editor, so it currently does not include:

- Save confirmation before creating a new file
- Unsaved changes detection
- Undo/Redo functionality
- Copy, Cut, and Paste menu options
- Find and Replace
- Multiple documents or tabs
- Support for advanced file formats

## Future Improvements

The project can be expanded by adding:

- Keyboard shortcuts such as `Ctrl + S` and `Ctrl + O`
- Undo and Redo
- Cut, Copy, and Paste
- Find and Replace
- Dark mode
- Word and character count
- Unsaved-changes warning
- Recent files
- Multiple tabs

## Author

Created as a basic Python GUI project using Tkinter.
