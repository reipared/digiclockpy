# Digital Clock

This code will create a digital clock using the Tkinter library in Python.

## Imports

```python
import tkinter as tk
import time
```

## Variables

```python
text_font = ("Boulder", 68, "bold")
background = "#f2e750"
foreground = "#363529"
border_width = 25
```

## Create the window

```python
app_window = tk.Tk()
app_window.title("Digital Clock")
app_window.geometry("420x150")
app_window.resizable(1, 1)
```

## Create the label

```python
label = tk.Label(app_window, font=text_font, bg=background, fg=foreground, bd=border_width)
label.grid(row=0, column=1)
```

## Create the function to update the clock

```python
def digital_clock():
    time_live = time.strftime("%H:%M:%S")
    label.config(text=time_live)
    label.after(200, digital_clock)
```

## Call the function to update the clock

```python
digital_clock()
```

## Start the main loop

```python
app_window.mainloop()
```

## Explanation

The first line of code, `import tkinter as tk`, imports the Tkinter library. The next line of code, `import time`, imports the time library.

The next section of code defines the variables that will be used to create the clock. The `text_font` variable specifies the font that will be used for the clock, the `background` variable specifies the background color for the clock, the `foreground` variable specifies the foreground color for the clock, and the `border_width` variable specifies the border width for the clock.

The next section of code creates the window for the clock. The `app_window` variable is created and assigned to a new Tkinter window. The `title()` method is used to set the title of the window, the `geometry()` method is used to set the size of the window, and the `resizable()` method is used to prevent the user from resizing the window.

The next section of code creates the label for the clock. The `label` variable is created and assigned to a new Tkinter label. The `font()` method is used to set the font for the label, the `bg()` method is used to set the background color for the label, the `fg()` method is used to set the foreground color for the label, and the `bd()` method is used to set the border width for the label. The label is then gridded in the window.

The next section of code creates the function to update the clock. The `digital_clock()` function gets the current time using the `time.strftime()` method and then sets the text of the label to the current time. The function then calls itself again after 200 milliseconds.

The next line of code calls the `digital_clock()` function to update the clock for the first time.

The last line of code starts the main loop for the Tkinter window. The main loop will continue to run until the user closes the window.
