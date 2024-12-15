# Uncommon HTML Bug: Handling Non-Existent Elements

This repository demonstrates a subtle bug in JavaScript within an HTML context. The code attempts to change the display style of an element that might not exist on the page.  This can lead to a silent error and unexpected behavior. The solution focuses on robust error handling to prevent such issues.

## Bug Description

The `myFunction` in `bug.html` hides a div with the id "myDiv", but then attempts to modify the display style of an element with the id "nonExistentElement." Since this element doesn't exist in the DOM, this action results in a silent JavaScript error.  The page won't crash, but the intended behavior (making "nonExistentElement" visible) won't occur.

## Solution

The `bugSolution.html` file presents a solution.  Before attempting to manipulate an element's style, it first checks if the element exists using `document.getElementById()`. If the element is not found (returns null), it gracefully handles the situation, preventing an error.