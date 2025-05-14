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
    <title>DOM Manipulation Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }

        button {
            padding: 10px;
            margin: 10px 0;
            cursor: pointer;
        }

        #dynamicContent p {
            background-color: #f0f0f0;
            padding: 10px;
            border: 1px solid #ccc;
        }

        #dynamicContent {
            margin-top: 20px;
        }

        .changed {
            color: red;
            font-weight: bold;
        }

        .bgColorChanged {
            background-color: #f0f8ff;
        }
    </style>
</head>
<body>

    <header>
        <h1>DOM Manipulation Example</h1>
    </header>

    <section>
        <p id="text">This is a paragraph. Click the button to change the text.</p>
        <button id="changeTextButton">Change Text</button>
    </section>

    <section>
        <p>Click the button to toggle background color.</p>
        <button id="toggleStyleButton">Toggle Background Color</button>
    </section>

    <section>
        <button id="addElementButton">Add New Element</button>
        <button id="removeElementButton">Remove Last Element</button>
        <div id="dynamicContent">
            <p>New elements will appear below.</p>
        </div>
    </section>

    <script>
        document.getElementById('changeTextButton').addEventListener('click', function() {
            let textElement = document.getElementById('text');
            textElement.textContent = "The text has been changed!";
            textElement.classList.add('changed');
        });

        document.getElementById('toggleStyleButton').addEventListener('click', function() {
            let body = document.body;
            body.classList.toggle('bgColorChanged');
        });

        document.getElementById('addElementButton').addEventListener('click', function() {
            let dynamicContent = document.getElementById('dynamicContent');
            let newElement = document.createElement('p');
            newElement.textContent = 'This is a newly added element!';
            dynamicContent.appendChild(newElement);
        });

        document.getElementById('removeElementButton').addEventListener('click', function() {
            let dynamicContent = document.getElementById('dynamicContent');
            if (dynamicContent.lastElementChild) {
                dynamicContent.removeChild(dynamicContent.lastElementChild);
            }
        });
    </script>

</body>
</html>

