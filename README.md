# Keycode Display Web App

This is a simple web application that displays the keycode and key name of any key pressed by the user. When a key is pressed, the application dynamically updates the display to show the name of the key and its corresponding keycode.
## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Usage](#usage)


## Introduction

This web application provides a visual representation of the key that you press on your keyboard, along with its corresponding keycode. It's a simple demonstration of capturing user input using JavaScript and updating the DOM in real-time.

## Features

- Real-time display of pressed keys and their keycodes.
- Simple and minimalist user interface.
- Easy-to-understand code structure.

## Usage

1. Open the web application in your preferred web browser.
2. As you press any key on your keyboard, the application will update to display the key name and its corresponding keycode.
3. The display will update dynamically as you press different keys.

## Step 1: HTML Code

The HTML code creates a simple container div with the class "container". This div will contain the input field and the button.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Keycode</title>

</head>
<body>
    <div class="container">
        <p>Enter Any KeyWord</p>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

## Step 2: CSS Code

The CSS code simply styles the container div.

```css
.container{
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-weight: 900;
    font-size: 40px;
}
p,h1{
    border: 2px solid rgb(91, 91, 91);
    box-shadow: 5px 10px #888888;
    padding: 10px 30px;
    margin-top: 10px;
    font-size: 40px;
}
```

## Step 3: JavaScript Code

The JavaScript code adds an event listener to the input field. When the user enters a keyword and presses the enter key, the keyword is displayed on the screen.

```javascript
let container = document.querySelector(".container");

document.addEventListener("keydown", function (event) {
    container.innerText = "";
    console.log(event);
  	let h1 = document.createElement("h1");
    h1.innerText = ` You Pressed  ${event.key}`;
    let p = document.createElement("p");
    p.innerText = `${event.keyCode}`;
    container.appendChild(h1);
    container.appendChild(p);


});
```
