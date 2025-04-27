# SVG Fill Rule Converter: Even-Odd to Non-Zero

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This is a simple HTML page designed to demonstrate or provide the functionality to convert the `fill-rule` attribute of SVG path elements from `evenodd` to `nonzero`.

## Why is this conversion needed?

The `fill-rule` attribute in SVG determines how to define the interior of a shape.

* **`evenodd`:** A ray is drawn from a point in any direction, and the number of path segment intersections with the ray is counted. If the number of intersections is odd, the point is inside; if even, it's outside.
* **`nonzero`:** A ray is drawn from a point in any direction, and the winding number is tracked. The winding number is determined by the direction in which each path segment crosses the ray (clockwise +1, counter-clockwise -1). If the total winding number is not zero, the point is inside.

When dealing with complex SVGs composed of multiple overlapping paths, `nonzero` often provides a more intuitive and predictable filling behavior.

## How to Use

1.  **Open the `index.html` file** (assuming your HTML file is named `index.html`): Open this HTML file directly in your web browser.
2.  **Upload SVG Icons:** Upload your SVG icons using the provided upload control on the page.
3.  **Click the Conversion Button:** Click the button on the page to start the conversion process.
4.  **View Conversion Results:** The converted SVG files will be available for batch saving.

## Features

This HTML page offers a straightforward interface to:

* Receive SVG code input from the user.
* Automatically detect and replace `fill-rule="evenodd"` with `fill-rule="nonzero"` in SVG path elements.
* Display the converted SVG code in real-time.

## Limitations

* Please ensure that SVG strokes are outlined before conversion.
* Currently, only the `fill-rule` attribute is targeted for conversion; other parts of the SVG code will remain unchanged.
* The tool might not handle highly complex or malformed SVG code correctly.

## Contribution

Feel free to report issues or suggest improvements by submitting issues.

## License

This project is open-sourced under the [MIT License](https://opensource.org/licenses/MIT).

---

This README file now describes your HTML-based SVG conversion tool in English. Remember to replace `index.html` with the actual name of your HTML file. If your HTML page has more specific features or interactions, be sure to elaborate on them in the "Features" section.
