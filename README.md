<img src="/rpp.png" width="200px">

# Real++ Interpreter

Real++ is a simple, high-level, interpreted language for creating graphical user interface (GUI) applications. It's designed to be easy to learn and use, allowing developers to create simple applications without writing complex Python or Tkinter code.

## Features

Real++ provides a set of straightforward commands to define and control your application's windows and widgets.

## Core Commands

| Command | Description | Example |
|---------|-------------|---------|
| `WINDOW` | Creates the main application window with a title. | `WINDOW "My App"` |
| `SIZE` | Sets the dimensions of the window. | `SIZE 600x400` |
| `ICON` | Sets the window's icon from a `.ico` file. | `ICON "realpp.ico"` |
| `LABEL` | Creates a text label on the window. | `LABEL greeting_label "Hello!" x=20 y=20` |
| `TEXTBOX` | Creates a text input field. | `TEXTBOX name_entry x=50 y=50` |
| `BUTTON` | Creates a clickable button. | `BUTTON my_btn "Click Me" x=100 y=100` |
| `VAR` | Defines a variable. | `VAR my_var = "initial value"` |
| `SET` | Updates the value of a variable or a widget property. | `SET my_var = "new value"` |
| `IF/ELSE` | Standard conditional logic. | `IF my_var == "a"` |
| `PRINT` | Outputs text to the terminal. | `PRINT "Debug message"` |
| `IMG` | Displays an image on the window. | `IMG my_logo "logo.png" x=200 y=20` |
| `BIND` | Links a code block to a specific event on a widget. | `BIND my_btn <Button-1>` |

## Example Code

Here is a full Real++ example demonstrating many of the language's features:

```rpp
WINDOW "Feature Showcase"
ICON "realpp.ico"
SIZE 600x400

# A red label with a bold font and a sunken border
LABEL my_label "Click me!" x=20 y=20 fg="red" font="Arial 16 bold" borderwidth=2 relief="sunken"

# A button with a green background
BUTTON my_button "Change Label" x=20 y=70 bg="green" width=150
SET my_label.fg = "blue"
SET my_label.value = "Color Changed!"
PRINT "Label color changed to blue."

# A bind command that changes the label on a left-click
BIND my_label <Button-1>
SET my_label.fg = "purple"
SET my_label.value = "Clicked!"

# A textbox with a lightblue background
TEXTBOX my_text x=20 y=120 bg="lightblue"

# An image added to the window (must exist in the same directory)
IMG my_image "logo.png" x=300 y=20
