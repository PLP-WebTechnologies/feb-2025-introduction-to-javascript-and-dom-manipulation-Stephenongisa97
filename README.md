# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Web Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to My Interactive Page</h1>
    </header>

    <main>
        <section>
            <p id="dynamicText">This text will change when you click the button below.</p>
            <button id="changeTextButton">Change Text</button>
        </section>

        <section>
            <button id="toggleColorButton">Toggle Background Color</button>
        </section>

        <section>
            <button id="addElementButton">Add New Element</button>
            <div id="dynamicContainer"></div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 My Interactive Page</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

// 1. Changing text content dynamically
const changeTextButton = document.getElementById("changeTextButton");
const dynamicText = document.getElementById("dynamicText");

changeTextButton.addEventListener("click", function() {
    dynamicText.textContent = "The text has been changed dynamically!";
});

// 2. Modifying CSS styles via JavaScript
const toggleColorButton = document.getElementById("toggleColorButton");
let isBackgroundRed = false;

toggleColorButton.addEventListener("click", function() {
    if (isBackgroundRed) {
        document.body.style.backgroundColor = "white";
    } else {
        document.body.style.backgroundColor = "red";
    }
    isBackgroundRed = !isBackgroundRed;
});

// 3. Adding or removing an element when a button is clicked
const addElementButton = document.getElementById("addElementButton");
const dynamicContainer = document.getElementById("dynamicContainer");

addElementButton.addEventListener("click", function() {
    const newElement = document.createElement("p");
    newElement.textContent = "A new paragraph element was added!";
    dynamicContainer.appendChild(newElement);
});



 






















