
<img src="/rpp.png" width="200">
# 🚀 Real++ Language Documentation

**Version:** 1.0
**Author:** rsamuelp aka. realsamuelp

Real++ is a high-level, interpreted language designed for rapid GUI app development. It’s simple, intuitive, and comes with built-in GUI components like windows, labels, buttons, textboxes, and images.

---

## 🖥️ 1. Creating a Window

```
WINDOW <id> size="<width>x<height>" bgcolor="<hex_color>" title="<window_title>"
```

* **id**: Identifier for the window.
* **size**: Dimensions (width x height).
* **bgcolor**: Background color in hex.
* **title**: (Optional) Window title.

**Example:**

```
WINDOW main size="400x300" bgcolor="#2C3E50" title="My App"
```

---

## 🔤 2. Labels

```
LABEL <id> "<text>" x=<x_pos> y=<y_pos> fg="<text_color>" bg="<bg_color>"
```

* **id**: Unique identifier.
* **text**: Displayed text.
* **x, y**: Position in pixels.
* **fg**: Text color.
* **bg**: Background color.

**Example:**

```
LABEL lblHello "Enter your name:" x=20 y=20 fg="#ECF0F1" bg="#2C3E50"
```

---

## ⌨️ 3. Textboxes

```
TEXTBOX <id> x=<x_pos> y=<y_pos> width=<width> height=<height> placeholder="<text>"
```

* **placeholder**: Text shown when empty.
* Access input using `.value`.

**Example:**

```
TEXTBOX txtName x=20 y=50 width=200 placeholder="Your name here"
```

---

## 🔘 4. Buttons

```
BUTTON <id> "<text>" x=<x_pos> y=<y_pos>
    <commands>
END
```

* Click event runs the commands inside the button block.
* Commands include `PRINT`, `SET`, arithmetic, or GUI updates.

**Example:**

```
BUTTON btnGreet "Greet" x=20 y=90
    PRINT "Hello, " & txtName.value & "!"
END
```

---

## 🖼️ 5. Images

```
IMG <id> "<file_path>" x=<x_pos> y=<y_pos> width=<width> height=<height>
```

* **file\_path**: Relative path to the image.
* Supports PNG, JPG.

**Example:**

```
IMG imgLogo "test.png" x=250 y=20 width=100 height=100
```

---

## 🟰 6. Dynamic Updates

* Change label or textbox values dynamically using `SET`.

```
SET <id>.text "<new_text>"
```

**Example:**

```
BUTTON btnUpdate "Update Label" x=20 y=130
    SET lblHello.text "Welcome, " & txtName.value
END
```

---

## 📊 7. Printing to Terminal

```
PRINT "<text>"  # Can include variables
```

**Example:**

```
PRINT "Hello, " & txtName.value
```

---

## 📝 8. Variables & Expressions

```
VAR count = 0
SET count = count + 1
PRINT "Button clicked " & count & " times"
```

* `VAR` declares a variable.
* `SET` updates variables or GUI elements.
* `&` concatenates strings.

---

## ⚡ 9. Conditional Statements

```
IF count > 5
    PRINT "High count!"
ELSE
    PRINT "Keep clicking..."
END
```

---

## 🔄 10. Loops

```
FOR i = 1 TO 5
    PRINT "Iteration " & i
END

WHILE count < 10
    PRINT count
    SET count = count + 1
END
```

---

## 🎉 11. Full Example

```
WINDOW main size="400x300" bgcolor="#2C3E50" title="Real++ Demo"

LABEL lblHello "Enter your name:" x=20 y=20 fg="#ECF0F1" bg="#2C3E50"
TEXTBOX txtName x=20 y=50 width=200 placeholder="Your name here"

BUTTON btnGreet "Greet" x=20 y=90
    PRINT "Hello, " & txtName.value & "!"
END

IMG imgLogo "test.png" x=250 y=20 width=100 height=100

BUTTON btnUpdate "Update Label" x=20 y=130
    SET lblHello.text "Welcome, " & txtName.value
END
```

---

This covers **most of Real++’s core features**: GUI elements, variables, loops, conditions, and dynamic updates.
Thanks for testing Real++ out!
