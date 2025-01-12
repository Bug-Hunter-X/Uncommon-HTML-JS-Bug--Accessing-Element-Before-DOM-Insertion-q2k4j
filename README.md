# Uncommon HTML/JavaScript Bug: Accessing Element Before DOM Insertion

This repository demonstrates a subtle bug that arises when JavaScript code attempts to interact with an HTML element before the element has been fully parsed and added to the Document Object Model (DOM).

## Bug Description
The bug occurs because the JavaScript code tries to access and modify the `innerHTML` of a `div` element (`myDiv`) before the browser has finished rendering the HTML. This often results in the `getElementById` method returning `null` or unexpected behavior.

## How to Reproduce
1. Open `bug.html` in a web browser.
2. Observe the console output.  You will likely see an error message or unexpected behavior.

## Solution
The solution involves ensuring that the JavaScript code interacts with the HTML element *after* the element has been fully loaded into the DOM. This is typically achieved by using the `DOMContentLoaded` event listener.

Check `bugSolution.html` for a corrected version that uses `DOMContentLoaded`.