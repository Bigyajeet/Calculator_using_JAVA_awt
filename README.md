# Calculator_using_JAVA_awt
A basic graphical calculator application built with Java AWT, providing fundamental arithmetic operations.
# Simple Java Calculator

This is a basic calculator application built using Java AWT (Abstract Window Toolkit). It allows users to perform simple arithmetic operations: addition, subtraction, multiplication, and division.

## Features

* **Basic Arithmetic Operations:** Supports addition (+), subtraction (-), multiplication (*), and division (/).
* **Clear Function:** Includes a "CLR" button to clear the input field.
* **Simple User Interface:** Uses a graphical user interface with buttons for digits and operations.

## How to Run

1.  **Save the code:** Save the provided Java code as `calculator.java`.
2.  **Compile the code:** Open a terminal or command prompt and navigate to the directory where you saved the file. Compile the code using the Java compiler:
    ```bash
    javac calculator.java
    ```
    This will generate a `calculator.class` file.
3.  **Run the application:** Execute the compiled class file using the Java Virtual Machine:
    ```bash
    java calculator
    ```
    This will open the calculator window.

## Usage

1.  **Enter numbers:** Click on the digit buttons (0-9) to enter the first number.
2.  **Select an operation:** Click on the desired operation button (+, -, *, /). The display will clear, ready for the second number.
3.  **Enter the second number:** Click on the digit buttons to enter the second number.
4.  **Calculate the result:** Click the "=" button to see the result in the display.
5.  **Clear the display:** Click the "CLR" button to reset the display to an empty string.

## Code Structure

The code is organized into a single Java class named `calculator`. It implements the `ActionListener` interface to handle button clicks.

* **Instance Variables:**
    * `c`, `n`: Integers used to store the current operation and the result.
    * `s1`, `s2`, `s3`, `s4`, `s5`: Strings used to handle input and display in the text field.
    * `f`: An instance of the `Frame` class, representing the main window.
    * `b0` to `b9`, `badd`, `bsub`, `bmul`, `bdiv`, `beq`, `bclr`: Instances of the `Button` class for the calculator's buttons.
    * `p`: An instance of the `Panel` class to hold the buttons.
    * `t1`: An instance of the `TextField` class for displaying input and results.
    * `g`: An instance of the `GridLayout` class to arrange the buttons in the panel.

* **Constructor (`calculator()`):**
    * Initializes the frame, panel, buttons, and text field.
    * Sets the layout for the frame (FlowLayout) and the panel (GridLayout).
    * Adds action listeners to all the buttons.
    * Adds the text field and panel to the frame.
    * Sets the size and visibility of the frame.
    * Sets the background color of the frame.
    * Adds a `WindowListener` to handle the closing of the window.

* **`actionPerformed(ActionEvent e)` Method:**
    * This method is called when any of the buttons are clicked.
    * It checks the source of the action event (`e.getSource()`) to determine which button was pressed.
    * For digit buttons (0-9), it appends the clicked digit to the text field.
    * For the operation buttons (+, -, \*, /), it stores the first operand (`s1`) and the selected operation (`c`), then clears the text field to prepare for the second operand.
    * For the equals button (=), it retrieves the second operand (`s2`), performs the stored operation based on the value of `c`, and displays the result in the text field.
    * For the clear button (CLR), it clears the text field.

* **`main(String[] args)` Method:**
    * This is the entry point of the program.
    * It creates an instance of the `calculator` class, which initializes and displays the calculator.

## Dependencies

This project uses the standard Java AWT library, which is included in the Java Development Kit (JDK). No external libraries are required.

## Potential Improvements

* **Error Handling:** Implement error handling for cases like division by zero or invalid input.
* **Decimal Numbers:** Add support for decimal numbers.
* **More Operations:** Include additional mathematical operations (e.g., square root, percentage).
* **User Interface Enhancements:** Improve the layout and appearance of the calculator.
* **Memory Functions:** Add memory recall, store, and clear functions.
