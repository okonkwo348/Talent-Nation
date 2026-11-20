# Cross-Platform Python Installation Guide

## Overview

Python is a beginner-friendly programming language used for web development, data science, artificial intelligence, automation, and many other applications.

This guide explains how to install Python on **Windows**, **macOS**, and **Linux**, verify that it is installed correctly, and run your first Python program.

> **Recommendation:** Always download Python from the official website:
> https://www.python.org/downloads/

---

# Windows

## Where to Get Python

Download Python from the official Python website:

https://www.python.org/downloads/

---

## Installation Steps

1. Open your web browser.
2. Visit **https://www.python.org/downloads/**.
3. Click the **Download Python** button.
4. Open the downloaded installer.
5. During installation:
   - Enable **Add Python to PATH** (if available).
   - Click **Install Now**.
6. Wait for the installation to finish.
7. Click **Close** when the installation is complete.

---

## Confirm Python Is Installed

1. Open **Command Prompt**.
2. Type:

```bash
python --version
```

If that does not work, try:

```bash
py --version
```

If Python is installed correctly, you should see something similar to:
Python 3.14.8

This means Python is successfully installed on your computer.

The 3.14.8 is the Python version number. Your version may be different.


---

## Run Your First Python Program

1. Open VS Code or Notepad.
2. Type:

```python
print("Hello, World!")
```

3. Save the file as `hello.py`.
4. Open your terminal in the folder where you saved the file.
5. Run:

```bash
python hello.py
```

If you are using Linux, run:

```bash
python3 hello.py
```

Expected output:

```text
Hello, World!
```

4. Open Command Prompt.
5. Navigate to the folder containing the file.

Example:

```bash
cd Desktop
```

6. Run the program:

```bash
python hello.py
```

or

```bash
py hello.py
```

Expected output:

```text
Hello, World!
```

---

# macOS

## Where to Get Python

Download the latest version from:

https://www.python.org/downloads/

Although macOS may include an older version of Python or none at all (depending on the version), beginners should install the latest official version from Python.org.
Even if your Mac already has Python installed, it is recommended to install the latest version from the official Python website. This ensures you are using the most recent and fully supported version of Python.

---

## Installation Steps

1. Open Safari or another web browser.
2. Visit **https://www.python.org/downloads/**.
3. Download the macOS installer.
4. Open the downloaded installer package.
5. Follow the installation instructions.
6. Wait until installation is complete.

---

## Confirm Python Is Installed

1. Open **Terminal**.
2. Type:

```bash
python3 --version
```

You should see something similar to:

```text
Python 3.x.x
```

---

## Run Your First Python Program

1. Open **TextEdit** and switch to plain text mode.
2. Type:

```python
print("Hello, World!")
```

3. Save the file as:

```
hello.py
```

4. Open Terminal.
5. Navigate to the folder where the file is saved.

Example:

```bash
cd Desktop
```

6. Run:

```bash
python3 hello.py
```

Expected output:

```text
Hello, World!
```

---

# Linux

## Where to Get Python

Most Linux distributions already include Python.

If Python is not installed, install it using your distribution's package manager or download it from the official Python website:

https://www.python.org/downloads/


---

## Installation Steps

### Ubuntu/Debian

Open a terminal and run:

```bash
sudo apt update
sudo apt install python3
```

### Fedora

```bash
sudo dnf install python3
```

### Arch Linux

```bash
sudo pacman -S python
```

---

## Confirm Python Is Installed

Open a terminal and type:

```bash
python3 --version
```

You should see:

```text
Python 3.x.x
```

---

## Run Your First Python Program

1. Open a text editor such as **Nano**, **VS Code**, or **Gedit**.
2. Create a file named:

```
hello.py
```

3. Add the following code:

```python
print("Hello, World!")
```

4. Save the file.
5. Open a terminal and navigate to the file's location.

Example:

```bash
cd ~/Desktop
```

6. Run:

```bash
python3 hello.py
```

Expected output:

```text
Hello, World!
```

---

# Summary

| Operating System | Download Source | Check Installation | Run Program |
|------------------|-----------------|--------------------|-------------|
| Windows | https://www.python.org/downloads/ | `python --version` or `py --version` | `python hello.py` |
| macOS | https://www.python.org/downloads/ | `python3 --version` | `python3 hello.py` |
| Linux | Package manager or https://www.python.org/downloads/ | `python3 --version` | `python3 hello.py` |

---

## Conclusion

After installing Python, verifying the installation, and successfully running a simple program, you are ready to begin learning Python programming. The same Python code works across Windows, macOS, and Linux, making it easy to develop applications on any major operating system.