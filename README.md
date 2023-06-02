# woman
This code is a Python script that uses the `turtle` module to draw shapes based on coordinates and colors extracted from a Microsoft Word document.

## Prerequisites
- Python 3.x
- `turtle` module
- `re` module
- `docx` module

## Installation
1. Make sure you have Python 3.x installed on your system.
2. Install the required modules by running the following command:
   ```
   pip install turtle docx
   ```

## Usage
1. Place the Word document you want to extract data from in the same directory as the script.
2. Set the `source` variable to the name of the Word document without the file extension.
   ```
   source = "woman"
   ```
3. Run the script using the command:
   ```
   python script.py
   ```
4. The script will extract coordinates and colors from the Word document and use them to draw shapes using the `turtle` module.

## Explanation
- The script starts by importing the necessary modules: `turtle`, `re`, and `docx`.
- The `source` variable is set to the name of the Word document without the file extension.
- The script opens the Word document specified by `source` using the `docx.Document()` function.
- It initializes two empty lists: `coordinates` and `colour`.
- The script iterates through each paragraph in the Word document.
  - It tries to extract coordinate and color information from each paragraph using regular expressions (`re` module).
  - If successful, it converts the extracted values to appropriate formats and appends them to the respective lists.
- It initializes a `Turtle` object called `pen` and a `Screen` object called `screen`.
- Various settings are applied to the `pen` and `screen` objects to configure the drawing environment.
- The script iterates through the extracted coordinates and colors.
  - For each set of coordinates and color, it sets the pen color and begins filling.
  - It then iterates through the individual coordinate pairs and draws lines accordingly.
  - After completing the shape, it ends the filling, hides the turtle, and moves to the next set of coordinates and colors.
- Finally, the script enters the main event loop using `screen.mainloop()`, which keeps the drawing window open until closed.

Feel free to modify the code according to your specific requirements and experiment with different Word documents and shapes to create interesting visualizations.
