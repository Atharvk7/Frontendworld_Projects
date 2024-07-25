

<div align="center">
  <br />
    <a href="" target="_blank">
      <img src="https://res.cloudinary.com/dswary0vy/image/upload/v1714314079/calculatoutput_gtcri5.png" alt="Project Banner" width="400px">
    </a>
  <br />

  <div>
    <img src="https://img.shields.io/badge/Html-black?style=for-the-badge&logoColor=white&logo=html&color=61DAFB" alt="html" />
    <img src="https://img.shields.io/badge/Css-black?style=for-the-badge&logoColor=white&logo=css&color=FD366E" alt="css" />
    <img src="https://img.shields.io/badge/Javascript-black?style=for-the-badge&logoColor=white&logo=javascript&color=06B6D4" alt="javascript" />
  </div>

  <h3 align="center">Calculator</h3>

   <div align="center">
     Welcome to our calculator project! Built with HTML, CSS, and JavaScript, it offers basic arithmetic operations with a user-friendly interface. Utilizing event handling and simple UI design, our calculator performs addition, subtraction, multiplication, and division. Ideal for quick calculations, it showcases the fundamentals of web development.
    </div>
</div>

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)
5. 🚀 [Usage](#usage)
6. 🕸️ [Explanation](#explanation)
7. 🔗 [Links](#links)

## <a name="introduction">🤖 Introduction</a>

<div align="center">
This repository contains the source code for a simple calculator application implemented in JavaScript. The calculator supports basic arithmetic operations like addition, subtraction, multiplication, and division.
</div>

<a href="https://www.linkedin.com/company/frontendworld/" target="_blank"><img src="https://github.com/sujatagunale/EasyRead/assets/151519281/618f4872-1e10-42da-8213-1d69e486d02e" /></a>

## <a name="tech-stack">⚙️ Tech Stack</a>
- HTML
- CSS
- JavaScript

## <a name="features">🔋 Features</a>

👉 **Addition:**: Perform addition of numbers.

👉 **Subtraction:**: Subtract one number from another.

👉 **Multiplication:**: Multiply two numbers together.

👉 **Division:**: Divide one number by another.

👉 **Clear Function:**: Reset the calculator display and clear all entries.

👉 **Responsive Design:**: Adapts to different screen sizes for mobile and desktop viewing.

👉 **User-Friendly Interface:**: Intuitive and easy-to-use interface for quick calculations.

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.

**Cloning the Repository**

```bash
git clone https://github.com/Atharvk7/Frontendworld_Projects.git
cd calculator
```

## <a name="usage">🚀 Usage</a>

<div align="center">
This repository contains the source code for a simple calculator application implemented in JavaScript. The calculator can perform basic arithmetic operations such as addition, subtraction, multiplication, and division.
</div>

<details>
<summary><code>HTML</code></summary>

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="style.css">
    <title>Calculator</title>
</head>

<body>
    <div class="container">
        

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>(</button></td>
                    <td><button>)</button></td>
                    <td><button>C</button></td>
                    <td><button>%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button>X</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button>-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button>.</button></td>
                    <td><button>/</button></td>
                    <td><button>=</button></td>
                </tr>
            </table>
        </div>
    </div>

</body>
<script src="index.js"></script>

</html>

```

</details>

<div>Include the following CSS in a file named <code>style.css</code>:</div>

<details>
<summary><code>CSS</code></summary>

```css
.container{
    text-align: center;
    margin-top:10px;
    background-color:#13695d;
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #244624;
    font-size:34px;
    height: 86px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: #978fa0;
    width: 90px;
    height: 77px;
    margin: 4px;
}

.calculator{ 
    border: 4px solid #13695d;
    background-color: #ff99f7;
    padding: 15px;
    border-radius: 40px;
    display: inline-block;
    
}


```

</details>

<div>Include the following JavaScript in a file named <code>index.js</code>:</div>

<details>
<summary><code>JAVASCRIPT</code></summary>

```javascript
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}


```

</details>

## <a name="explanation">🕸️ Explanation</a>

**1. HTML Structure**: 
<ul>
  <li>The HTML defines the structure of the calculator, including the display and buttons for digits and operations.</li>
  <li>The display is an input field where the calculation is shown.</li>
</ul>

**2. CSS Styling**: 
<ul>
  <li>The CSS styles the calculator, providing a clean and modern look with responsive design elements.</li>
  <li>Buttons and the display are styled for easy interaction and visibility.</li>
</ul>

**3. JavaScript Functionality**: 
<ul>
  <li><code>Event Listener for Buttons</code>: Iterates over all buttons, adding a click event listener to handle user interactions.</li>
  <li><code>Button Text Handling</code>: Captures the text displayed on the clicked button.</li>
  <li><code>Multiplication ('X')</code>: Converts 'X' to '*' (multiplication operator) and appends it to the display.</li>
  <li><code>Clear ('C')</code>: Resets the display and the current input to an empty string.</li>
  <li><code>Equals ('=')</code>: Evaluates the mathematical expression in the display and shows the result.</li>
  <li><code>Default Case</code>: Appends the clicked button's text (number or operator) to the display.</li>
</ul>

## <a name="links">🔗 Links</a>
Live Project can be found [here](https://calculator-byfrontendworld.netlify.app/)

