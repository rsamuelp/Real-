<img src="/rpp.png" width="200px">

# 🚀 Real++ Interpreter  

🎉 **Real++ v1.0 is here** — a brand-new, high-level interpreted language for building **GUI apps** with simple, readable commands. No messy Python boilerplate, no Tkinter headaches. Just type, run, and flex your creation.  

---

## ✨ Features

- 🪟 **Window Management** – build apps with windows, icons, labels, and buttons  
- 🎨 **Custom Styling** – colors, fonts, borders, and more  
- 🖼️ **Image Support** – add images and icons directly  
- ⚡ **Events & Logic** – `BIND`, `IF/ELSE`, variables, and `SET` for interactivity  
- 🛠️ **Beginner Friendly** – learn it in minutes, build something in seconds  

---

## 🧩 Core Commands

| Command   | Description | Example |
|-----------|-------------|---------|
| `WINDOW`  | Creates the main application window with a title. | `WINDOW "My App"` |
| `SIZE`    | Sets the dimensions of the window. | `SIZE 600x400` |
| `ICON`    | Sets the window's icon from a `.ico` file. | `ICON "realpp.ico"` |
| `LABEL`   | Creates a text label on the window. | `LABEL greeting "Hello!" x=20 y=20` |
| `TEXTBOX` | Creates a text input field. | `TEXTBOX name_entry x=50 y=50` |
| `BUTTON`  | Creates a clickable button. | `BUTTON my_btn "Click Me" x=100 y=100` |
| `VAR`     | Defines a variable. | `VAR my_var = "initial value"` |
| `SET`     | Updates a variable or widget property. | `SET my_var = "new value"` |
| `IF/ELSE` | Conditional logic. | `IF my_var == "a"` |
| `PRINT`   | Prints text to the terminal. | `PRINT "Debug message"` |
| `IMG`     | Displays an image. | `IMG logo "logo.png" x=200 y=20` |
| `BIND`    | Attaches code to widget events. | `BIND my_btn <Button-1>` |

---

## 🚀 Example App (Full Demo)

```rpp
WINDOW "Feature Showcase"
ICON "realpp.ico"
SIZE 600x400

# A red label with bold font & sunken border
LABEL my_label "Click me!" x=20 y=20 fg="red" font="Arial 16 bold" borderwidth=2 relief="sunken"

# A button that changes the label color
BUTTON my_button "Change Label" x=20 y=70 bg="green" width=150
SET my_label.fg = "blue"
SET my_label.value = "Color Changed!"
PRINT "Label color changed to blue."

# Bind: label reacts on left-click
BIND my_label <Button-1>
SET my_label.fg = "purple"
SET my_label.value = "Clicked!"

# A textbox
TEXTBOX my_text x=20 y=120 bg="lightblue"

# Display an image
IMG my_image "logo.png" x=300 y=20
