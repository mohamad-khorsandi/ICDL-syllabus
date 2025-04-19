### 📝 1. **Hello World Script**

**Goal**: Print a message to the screen.

```
batCopy code@echo off
echo Hello, World!
pause
```

**Explanation**:

- `@echo off`: Hides the command being executed (makes output cleaner).
- `echo`: Displays text to the screen.
- `pause`: Waits for the user to press a key before closing.

------

### 🗂️ 2. **Creating a Folder**

**Goal**: Create a folder (e.g. `NewFolder`).

```
batCopy code@echo off
mkdir NewFolder
pause
```

**Explanation**:

- `mkdir`: Creates a new directory/folder.
- `pause`: Waits for user input before closing.

------

### 📋 3. **Simple File Copy**

**Goal**: Copy a file from one folder to another.

```
batCopy code@echo off
copy "C:\path\to\source\file.txt" "C:\path\to\destination\file.txt"
pause
```

**Explanation**:

- `copy`: Copies files from one location to another.
- `pause`: Lets you see the result before closing.

------

### 🖱️ 4. **Opening a Program**

**Goal**: Launch a program (e.g., Notepad).

```
batCopy code@echo off
start notepad.exe
pause
```

**Explanation**:

- `start`: Launches the specified program (in this case, Notepad).
- `pause`: Allows you to see the result and not immediately close the script.

------

### 🔄 5. **Simple Loop**

**Goal**: Print numbers from 1 to 5.

```
batCopy code@echo off
for /l %%i in (1,1,5) do (
  echo %%i
)
pause
```

**Explanation**:

- `for /l %%i in (start, step, end)`: Loops through a range of numbers.
- `%%i`: The loop variable (a number in this case).
- `echo %%i`: Prints each number during the loop.
- `pause`: Waits for user input before closing.

------

### 📅 6. **Display the Current Date and Time**

**Goal**: Show the current system date and time.

```
batCopy code@echo off
echo The current date is: %date%
echo The current time is: %time%
pause
```

**Explanation**:

- `%date%` and `%time%`: System variables that contain the current date and time.
- `pause`: Lets you view the result.

------

### 🧹 7. **Deleting a File**

**Goal**: Delete a specific file.

```
batCopy code@echo off
del "C:\path\to\file.txt"
pause
```

**Explanation**:

- `del`: Deletes a file at the given path.
- `pause`: Lets you confirm the deletion before closing.

------

### 🔑 8. **Prompt for User Input**

**Goal**: Ask the user for their name and greet them.

```
batCopy code@echo off
set /p name=Enter your name: 
echo Hello, %name%!
pause
```

**Explanation**:

- `set /p`: Prompts the user to enter data.
- `%name%`: Uses the entered value.
- `echo`: Prints the result.

------

### 🔒 9. **Check if a Folder Exists**

**Goal**: Check if a folder exists, and create it if not.

```
batCopy code@echo off
if not exist "C:\path\to\folder" (
    mkdir "C:\path\to\folder"
    echo Folder created!
) else (
    echo Folder already exists.
)
pause
```

**Explanation**:

- `if not exist`: Checks if the folder exists.
- `mkdir`: Creates the folder if it doesn't exist.
- `pause`: Lets you see the result.

------

### 🧑‍💻 10. **Open Multiple Programs**

**Goal**: Open several programs at once.

```
batCopy code@echo off
start notepad.exe
start calc.exe
start mspaint.exe
pause
```

**Explanation**:

- `start`: Launches the programs simultaneously.
- `pause`: Lets you see the result.

------

### 🧠 **Summary of Common Batch Commands**:

- `@echo off`: Turns off command display for cleaner output.
- `echo`: Displays messages.
- `pause`: Waits for user interaction before closing.
- `mkdir`: Creates directories/folders.
- `copy`: Copies files.
- `del`: Deletes files.
- `start`: Opens programs or websites.
- `for`: Loops (used for repetition).
- `set /p`: Prompts the user for input.
- `if`: Conditional checks.