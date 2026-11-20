# 🛠️ Python Troubleshooting Desk: Beginner's Fix-It Guide

Setting up Python for the first time can feel frustrating when a command fails or a script throws an error. Use this guide to diagnose what went wrong and get back on track quickly.

---

## 1. Python Installation

### Problem: The installer finishes, but typing `python` in the terminal gives an error or opens the Microsoft Store
* **What Happens:** You install Python, open a terminal, type `python --version`, and get `'python' is not recognized as an internal or external command` (on Windows) or the Microsoft Store pops up instead of running Python.
* **Possible Cause:** On Windows, the **"Add python.exe to PATH"** box wasn't checked during installation, so Windows doesn't know where to find `python.exe`. (On macOS and Linux, the command is often `python3` rather than `python`.)
* **How to Resolve It:**
  1. Re-run the official Python installer from [python.org](https://www.python.org/downloads/).
  2. Click **Modify** (or **Repair**).
  3. On the next screen, make sure **Add Python to environment variables** is checked, then finish the setup.
  4. Close and reopen your terminal, then test again with `python --version` (or `python3 --version` on macOS/Linux).

---

## 2. Environment Setup

### Problem: A virtual environment won't activate, or `(.venv)` doesn't show up in your prompt
* **What Happens:** You create a virtual environment (`python -m venv .venv`), try to activate it, and either get a permission/execution error or your terminal prompt doesn't change to show `(.venv)`.
* **Possible Cause:** You used the wrong activation command for your operating system or shell (for example, running a Linux/macOS `source` command in Windows PowerShell, or PowerShell's script execution policy blocks `.ps1` scripts).
* **How to Resolve It:**
  1. Make sure you are inside the folder that contains `.venv`.
  2. Run the activation command that matches your shell:
     * **Windows (Command Prompt):** `.venv\Scripts\activate.bat`
     * **Windows (PowerShell):** `.venv\Scripts\Activate.ps1` (if blocked, run `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser` first, then activate again).
     * **macOS / Linux (Bash/Zsh):** `source .venv/bin/activate`
  3. Confirm you see `(.venv)` at the start of your terminal line before running further commands.

---

## 3. Package Installation

### Problem: `pip install <package>` fails with a `ModuleNotFoundError: No module named pip` or permission denied error
* **What Happens:** You try to install a library (like `requests` or `pytest`) and `pip` fails with a missing-module error or a system permission/externally-managed error.
* **Possible Cause:** Either `pip` isn't installed/up to date in that environment, or you are trying to install packages into a protected global/system Python directory instead of an isolated virtual environment.
* **How to Resolve It:**
  1. Activate your project's virtual environment first (`source .venv/bin/activate` or `.venv\Scripts\activate`).
  2. Ensure `pip` is available and updated using Python's module flag:
     ```bash
     python -m ensurepip --upgrade
     python -m pip install --upgrade pip
     ```
  3. Install your package inside that active environment:
     ```bash
     python -m pip install requests
     ```

---

## 4. Running Python

### Problem: Running `python` launches an older Python version than the one you just installed
* **What Happens:** You installed a newer Python 3 release, yet typing `python` or `python3` opens an older version.
* **Possible Cause:** Multiple Python installations exist on your machine, and an older version appears earlier in your system `PATH` or is selected by your editor/IDE.
* **How to Resolve It:**
  1. Check which executable is being called:
     * **Windows:** `where python` (or use `py -3` with the Python launcher)
     * **macOS / Linux:** `which -a python3`
  2. If using VS Code or another IDE, open the Command Palette / interpreter selector and pick the newer Python version or your `.venv` interpreter.
  3. If needed, update your system `PATH` so the newer Python installation comes first, then open a fresh terminal.

---

## 5. Running a Python Script

### Problem: Running `python hello.py` fails with `No such file or directory` (or `can't open file`) or immediately throws a `SyntaxError`
* **What Happens:** You try to run your script and either Python says it can't find the file, or it stops immediately with a `SyntaxError` before printing anything.
* **Possible Cause:**
  * **File not found:** Your terminal is in a different folder than `hello.py`, or the file was saved as `hello.py.txt` by a text editor.
  * **SyntaxError:** Your code has a structural grammar mistake (such as a missing closing parenthesis `)`, missing quote, or missing colon `:`), which stops Python during compilation before execution begins.
* **How to Resolve It:**
  1. **For missing files:** List files in your current folder (`dir` on Windows, `ls` on macOS/Linux) and use `cd` to move into the folder where `hello.py` is saved. Check that it isn't named `hello.py.txt`.
  2. **For `SyntaxError`:** Read the line number and caret (`^`) pointer in the error message, check that line and the line right above it for unclosed quotes/parentheses or missing colons, save the file, and run it again.

---

### 💡 Quick Debugging Habit
Whenever something breaks, read the **last line of the error message first** to see what went wrong, and check the **line number** right above it to see where Python ran into trouble.