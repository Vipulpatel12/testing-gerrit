# Code Documentation for Python Function: `system`
## Overview
This function in python is used to execute a command. It doesn't return any value and takes one parameter which is the command that you want to run on your system. 
## Inputs
The only input this function requires is the string of a command you want executed on your local machine. This should be provided as the argument for the `system` function itself. The command could be anything like creating directories, deleting files etc., which are all performed using shell commands in Linux/Unix based systems. 
## Outputs
The outputs of this function are usually printed to the console where you're running your script or Jupyter notebook, if it is used within a python environment. If you need to capture these outputs into your program for further use, consider using the subprocess module which can interact with operating system commands and return their output as string.
## Example Usage
```python
import os
os.system('dir')  # This will execute 'dir' command in windows cmd
os.system("ls")   # This will execute 'ls' command in Unix/Linux terminal
```
