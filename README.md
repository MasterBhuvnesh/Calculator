# Calculator
A  Desktop 💻  based calculator Application made with the help of Tkinter and Python ..

## Documentation

```python
import tkinter as tk
```
This line imports the tkinter module, which is a standard Python interface to the Tk GUI toolkit. It is used to create graphical user interfaces.

```python
LARGE_FONT_STYLE = ("Arial", 40, "bold")
SMALL_FONT_STYLE = ("Arial", 16)
DIGITS_FONT_STYLE = ("Arial", 24, "bold")
DEFAULT_FONT_STYLE = ("Arial", 20)
```
Here, several font styles are defined using tuples. These font styles will be used to set the appearance of various text elements in the GUI.


```python
OFF_WHITE = "#F8FAFF"
WHITE = "#FFFFFF"
LIGHT_BLUE = "#CCEDFF"
LIGHT_GRAY = "#F5F5F5"
LABEL_COLOR = "#25265E"
```
These lines define color codes using hexadecimal values. These colors are used to set the background and text colors of different GUI elements.


```python
class Calculator:
```
This defines a class named Calculator that encapsulates the functionality of the calculator GUI.

```python
def __init__(self):
```    
The __init__ method is the constructor of the Calculator class. It is executed when an instance of the class is created. It initializes various attributes and sets up the initial state of the calculator GUI.

```python
self.window = tk.Tk()
```
This line creates the main application window using the Tk class from the tkinter module.

```python
self.window.geometry("375x667")
```
This sets the initial dimensions of the window to 375 pixels in width and 667 pixels in height.

```python
self.window.iconbitmap("calculator.ico")
```
This line sets the icon for the application window to a file named "calculator.ico". The icon file should be present in the same directory as the script.


```python
self.window.resizable(0, 0)
```
This disables the ability to resize the window by setting the resizable method's arguments to (0, 0).


```python
self.window.title("Calculator")
```
This sets the title of the application window to "Calculator".


```python
self.total_expression = ""
self.current_expression = ""
```
These attributes are used to store the total and current expressions being entered into the calculator.


```python
self.display_frame = self.create_display_frame()
```
This line calls the create_display_frame method to create a frame that will contain the display area of the calculator.


```python
self.total_label, self.label = self.create_display_labels()
```
Here, the create_display_labels method is called to create two labels for displaying the total and current expressions. The labels are assigned to the total_label and label attributes.



```python
self.digits = {
    7: (1, 1), 8: (1, 2), 9: (1, 3),
    4: (2, 1), 5: (2, 2), 6: (2, 3),
    1: (3, 1), 2: (3, 2), 3: (3, 3),
    0: (4, 2), '.': (4, 1)
}
```
This dictionary self.digits maps digit values and the decimal point to their corresponding grid positions in the calculator layout. The format (row, column) is used to specify the position of each digit button.

```python
self.operations = {"/": "\u00F7", "*": "\u00D7", "-": "-", "+": "+"}
```
The self.operations dictionary maps arithmetic operators to their corresponding symbols for display. Unicode characters are used for division and multiplication symbols.


```python
self.buttons_frame = self.create_buttons_frame()
```
This line calls the create_buttons_frame method to create a frame that will contain all the calculator buttons.

```python
self.buttons_frame.rowconfigure(0, weight=1)
for x in range(1, 5):
    self.buttons_frame.rowconfigure(x, weight=1)
    self.buttons_frame.columnconfigure(x, weight=1)
    ```
Here, the rowconfigure and columnconfigure methods are used to configure the layout of the button frame. These methods ensure that the rows and columns expand and fill the available space evenly.


```python
self.create_digit_buttons()
self.create_operator_buttons()
self.create_special_buttons()
```
These lines call methods to create the digit buttons, operator buttons, and special buttons like "C", "x²", and "√".

```python
self.bind_keys()
```
This method is called to set up key bindings for keyboard input. It binds keys like digits, operators, and Enter to their corresponding calculator actions.


```python
def run(self):
    self.window.mainloop()
 ```   
This method starts the main event loop of the Tkinter application, which keeps the GUI running and responsive to user interactions.


```python
if __name__ == "__main__":
    calc = Calculator()
    calc.run()
```
This block of code checks if the script is being run directly (as opposed to being imported as a module). If it's the main execution, it creates an instance of the Calculator class and starts the GUI application using the run method.

## 👀 Screenshots of Application


![Screenshotcalculator](https://github.com/MasterBhuvnesh/Calculator/assets/99537126/1860a9a7-a445-47e0-9bf7-1881882196f2)


## 👀 Screenshots of Code


![image](https://github.com/MasterBhuvnesh/Calculator/assets/99537126/0eda5fb0-e433-49a2-8768-436afc2f131f)


## 🔗 Links

[![linkedin](https://img.shields.io/badge/instagram-FF007F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/verma_bhuvnesh_2904/)

[![linkedin](https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white)](https://www.instagram.com/bhuvnesh_2904/)
