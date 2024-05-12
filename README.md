# Ex.08 Design of a Standard Calculator
## Date:12-05-2024

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
### HTML
```html
<!DOCTYPE html>
<html>
<head>
    <title>CALCULATOR</title>
    <link rel="stylesheet" href="b.css">
</head>
<body style="background-color: rgb(227, 173, 166);">
    <div id="cal">
        <input  id="display" readonly>
        <div id="key">
            
            <button onclick="appendToDisplay('1')" >1</button>
            <button onclick="appendToDisplay('2')" >2</button>
            <button onclick="appendToDisplay('3')" >3</button>
            <button onclick="appendToDisplay('+')" class="operator-btn">+</button>

            <button onclick="appendToDisplay('4')" >4</button>
            <button onclick="appendToDisplay('5')" >5</button>
            <button onclick="appendToDisplay('6')" >6</button>
            <button onclick="appendToDisplay('-')" class="operator-btn">-</button>
            

            <button onclick="appendToDisplay('7')" >7</button>
            <button onclick="appendToDisplay('8')" >8</button>
            <button onclick="appendToDisplay('9')" >9</button>
            <button onclick="appendToDisplay('*')" class="operator-btn">*</button>
            
            <button onclick="cleardisplay()" class="operator-btn">C</button>
            <button onclick="appendToDisplay('0')" >0</button>
            <button onclick="appendToDisplay('.')" >.</button>
            <button onclick="appendToDisplay('/')" class="operator-btn">/</button>
            <button onclick="calculate()" class="a operator-btn">=</button>


            
        </div>
    </div>
    <script src="c.js"></script>
</body>
</html>
```

### CSS
```css
button {
    width: 100px;
    height: 100px;
    border-radius: 50px;
    border: none;
    background-color: hsl(0, 0%, 100%);
    color: rgb(0, 0, 0);
    font-size: 3rem;
    font-weight: bold;
    cursor: pointer;
}

button:hover {
    background-color: rgb(255, 255, 255);
    transition: 2s;
}

button:active {
    background-color: rgb(0, 0, 0);
}

#key {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    padding: 25px;
}

#cal {
    font-family: 'Times New Roman';
    background-color: rgb(0, 0, 0);
    border-radius: 20px;
    max-width: 470px;
    overflow: hidden;
    color: rgb(0, 0, 0);
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

#display {
    width: 100%;
    padding: 20px;
    font-size: 5rem;
    text-align: left;
    border: none;
    background-color: hsl(0, 0%, 0%);
    color: rgb(255, 255, 255);
}

body {
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: white;
}

.operator-btn {
    background-color: hsl(173, 4%, 59%);
}

.operator-btn:hover {
    background-color: hsl(0, 0%, 0%);
}

.operator-btn:active {
    background-color: hsl(0, 0%, 0%);
}
#key {
    justify-content: end;
}
.a{
    position: relative;
    top: 10px;
    left: 330px;
}
.b{
    position: relative;
    left: 10px;
    top:5px;
}
```

### JS
```js
var display = document.getElementById("display");

function appendToDisplay(input) {
    display.value += input;
}

function cleardisplay() {
    display.value = "";
}

function calculate() {
    try {
        display.value = eval(display.value);
    } catch(error) {
        display.value = "Error";
    }
}
```

## OUTPUT:
![alt text](<Screenshot (338).png>)

![alt text](<Screenshot (339).png>)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
