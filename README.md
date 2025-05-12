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
    <title>Interactive Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to My Interactive Page</h1>
    </header>

    <section id="content">
        <p>This is some static text.</p>
        <p id="dynamic-text">This text will change when you click the button.</p>
    </section>

    <button id="change-text-btn">Change Text and Style</button>
    <button id="add-remove-element-btn">Add/Remove Element</button>

    <footer>
        <p>&copy; 2025 My Interactive Website</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>


body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f9;
}

header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 20px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    width: 100%;
    bottom: 0;
}

button {
    margin: 10px;
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

// Change the text content dynamically
const changeTextButton = document.getElementById('change-text-btn');
const dynamicText = document.getElementById('dynamic-text');

changeTextButton.addEventListener('click', function() {
    dynamicText.textContent = "The text has been changed!";
    dynamicText.style.color = 'blue'; // Modifying CSS style dynamically
    dynamicText.style.fontWeight = 'bold';
});

// Add or remove an element when a button is clicked
const addRemoveElementButton = document.getElementById('add-remove-element-btn');
const contentSection = document.getElementById('content');

addRemoveElementButton.addEventListener('click', function() {
    let newElement = document.createElement('p');
    newElement.textContent = "A new element has been added!";
    newElement.style.color = 'red';

    if (contentSection.contains(newElement)) {
        contentSection.removeChild(newElement);
    } else {
        contentSection.appendChild(newElement);
    }
});




















