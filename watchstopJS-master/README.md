



<div align="center">
  <br />
    <a href="" target="_blank">
      <img src="https://res.cloudinary.com/dslzeoxj7/image/upload/v1720807183/stopwatch_hcibbp.png" alt="Project Banner">
    </a>
  <br />

  <div>
    <img src="https://img.shields.io/badge/Html-black?style=for-the-badge&logoColor=white&logo=html&color=61DAFB" alt="html" />
    <img src="https://img.shields.io/badge/Css-black?style=for-the-badge&logoColor=white&logo=css&color=FD366E" alt="css" />
    <img src="https://img.shields.io/badge/Javascript-black?style=for-the-badge&logoColor=white&logo=javascript&color=06B6D4" alt="nativewind" />
  </div>

  <h3 align="center">Stopwatch</h3>

   <div align="center">
     Welcome to our stopwatch project! Crafted with HTML, CSS, and JavaScript, it accurately measures time. Utilizing asynchronous JS, event handling, and Date methods, our stopwatch offers precision. Ideal for timing laps or study sessions, it showcases web tech's power. Explore how async JS and events ensure accuracy in timekeeping!
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

<div  align="center">
This repository contains the source code for a simple stopwatch application implemented in JavaScript. The stopwatch can start, pause, and stop the time, displaying hours, minutes, seconds, and milliseconds.

</div>



<a href="https://www.linkedin.com/company/frontendworld/" target="_blank"><img src="https://github.com/sujatagunale/EasyRead/assets/151519281/618f4872-1e10-42da-8213-1d69e486d02e" /></a>


## <a name="tech-stack">⚙️ Tech Stack</a>
- HTML
- CSS
- Javascript

## <a name="features">🔋 Features</a>

👉 **Start Timer**: Begins the stopwatch from zero.

👉 **Pause Timer:**:  Pauses the stopwatch without resetting the time.

👉 **Stop Timer:**: Stops the stopwatch and resets the time to zero.

👉 **Accurate Timing:**: Tracks time down to milliseconds.

👉 **Responsive Display:**: Dynamically updates the display to show hours, minutes, seconds, and milliseconds.

👉 **Easy to Integrate:**: Simple and easy to integrate into any web project.

👉 **User-Friendly Interface:**: Intuitive buttons for starting, pausing, and stopping the timer.

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.


**Cloning the Repository**

```bash
git clone https://github.com/Atharvk7/Frontendworld_Projects.git
cd Frontendworld_Projects
```

## <a name="usage">🚀 Usage</a>
<div align="center">
This repository contains the source code for a simple stopwatch application implemented in JavaScript. The stopwatch can start, pause, and stop the time, displaying hours, minutes, seconds, and milliseconds.

</div>

<details>
<summary><code>HTML</code></summary>

```html
<!DOCTYPE html>
<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="shortcut icon" href="images/ws.png" type="image/x-icon">
    <link rel="stylesheet" href="style.css">
    <title>Stopwatch</title>
</head>
<body>
    <header>
        <h1>Stopwatch</h1>
    </header>
    <main>
        <section>
            <h2 id="timer">00:00:00<span id="millisecond">:00</span></h2>
            <article>
                <button id="start">Start</button>
                <button id="pause">Pause</button>
                <button id="stop">Stop</button>
            </article>
        </section>
    </main>
    <footer>
        <p>By FrontendWorld</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
```

</details>



<div>Include the following css in a file named style.js:</div>

<details>
<summary><code>CSS</code></summary>

```css
:root {
    --transparent-black : rgba(0, 0, 0, 0.445);
    --red: rgb(235, 15, 15);
    --green: rgb(30, 184, 30);
    --gray: rgb(211, 211, 211);
    --dark-color: #111;
    --font-color: #f0ece2;;
}

* {
    box-sizing: border-box;
}

html, body {
    margin: 0px;
    padding: 0px;
    font-family: Arial, Helvetica, sans-serif;
}

body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: var(--dark-color);
}

header, footer {
    color: var(--font-color);
}

section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 5px;
    padding-bottom: 5px;
    border-radius: 20px;
    box-shadow: 1px 1px 10px var(--transparent-black);
    width: 500px;
    background-color: whitesmoke;
}

article {
    display: flex;
    flex-direction: row;
}

h2 {
    font-size: 65pt;
}

#millisecond {
    font-size: 32pt;
}

#start, #pause, #stop {
    border: none;
    width: 120px;
    height: 120px;
    border-radius: 50%;
    margin: 15px;
    font-size: 18pt;
    text-transform: uppercase;
    font-weight: bold;
    cursor: pointer;
    opacity: 1;
}

#start:hover, #pause:hover, #stop:hover {
    opacity: 0.8;
    box-shadow: -1px -1px 1px var(--transparent-black),
                1px 1px 1px var(--transparent-black);
}

#start {
    background-color: var(--green);
}

#pause {
    background-color: var(--gray);
}

#stop {
    background-color: var(--red);
}
```

</details>


<div>Include the following JavaScript in a file named script.js:</div>
<details>
<summary><code>JAVASCRIPT</code></summary>

```javascript
let startBtn = document.querySelector('#start').addEventListener ('click', toStart,);
let pauseBtn = document.querySelector('#pause').addEventListener ('click', toPause);
let stopBtn = document.querySelector('#stop').addEventListener ('click', toStop);

let hour = 0;
let min = 0;
let sec = 0;
let ms = 0;
const time = 10;
let stopwatchActivity = 'none';
let stopwatch;


function toStart() {
  if (stopwatchActivity == 'none') {
    stopwatch = setInterval(() => { timer() }, time);
    stopwatchActivity = 'active';
  } else {}
}

function toPause() {
  clearInterval(stopwatch);
  stopwatchActivity = 'none';
}

function toStop() {
  stopwatchActivity = 'none';
  clearInterval(stopwatch);
  hour = 0;
  min = 0;
  sec = 0;
  ms = 0
  document.querySelector('#timer').innerHTML = '00:00:00<span id="millisecond">:00</span>';
}

function timer() {
  ms++;

  if (ms == 100) { ms = 0; sec++ }
  
  if (sec == 60) { sec = 0; min++; }

  if (min == 60) { min = 0; hour++; }

  let visualTimer = `${(hour < 10 ? `0${hour}` : hour)}:${(min < 10 ? `0${min}` : min)}:${(sec < 10 ? `0${sec}` : sec)}<span id="millisecond">:${ms < 10 ? `0${ms}` : ms}</span>`;
  document.querySelector('#timer').innerHTML = visualTimer;
}
```

</details>







## <a name="explanation">🕸️Explanation</a>
**1.Variables and Event Listeners**: 
<ul>
  <li>Event listeners are added to the buttons to call the respective functions when clicked.</li>
  <li>Variables are initialized to keep track of hours, minutes, seconds, and milliseconds.</li>
</ul>

**2.toStart Function:**: 
<ul>
  <li>Starts the timer if it's not already running by setting an interval that calls the timer function every 10 milliseconds.</li>
  <li>Updates the stopwatchActivity to 'active'</li>
</ul>

**3.toPause Function:**: 
<ul>
  <li>Pauses the timer by clearing the interval.</li>
  <li>Updates the stopwatchActivity to 'none'.</li>
</ul>

**4.toStop Function:**: 
<ul>
  <li>Stops the timer and resets all time variables to zero.</li>
  <li>Updates the displayed timer to '00:00:00:00'.</li>
</ul>

**5.timer Function:**: 
<ul>
  <li>Increments the milliseconds count.</li>
  <li>Updates seconds, minutes, and hours accordingly.</li>
  <li>Updates the displayed timer with the current time.</li>
</ul>

## <a name="links">🔗 Links</a>
Live Project can be found [here](https://frontendworld.io/)



















