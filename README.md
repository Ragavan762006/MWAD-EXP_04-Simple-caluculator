# MWAD-EXP_04-Simple-caluculator
## Name : Ragavan E
## Reg No: 212223040160
## Date: 21/9/2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
## App.jsx
```
import React from 'react';
import Calculator from './Calculator';

function App() {
  return (
    <div className="App">
      <h1>Simple Calculator</h1>
      <Calculator />
    </div>
  );
}

export default App;

```
## Calculator.jsx
```
import React, { useState } from 'react';
import './Calculator.css';

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => setInput(input + value);
  const handleClear = () => setInput("");
  const handleCalculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <input type="text" value={input} readOnly />
      <div className="buttons">
        <button onClick={handleClear}>C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={() => handleClick("-")}>-</button>
        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>
        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={handleCalculate}>=</button>
        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("0")}>0</button>
        <button onClick={() => handleClick(".")}>.</button>
      </div>
    </div>
  );
}

export default Calculator;

```
## Calculator.css
```

.calculator {
  width: 220px;
  margin: 50px auto;
  border: 2px solid black;
  padding: 20px;
  border-radius: 10px;
  background: #f9f9f9; 
  
}

input {
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  text-align: right;
  font-size: 18px;
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 50px);
  grid-gap: 10px;
}

button {
  width: 50px;
  height: 50px;
  font-size: 18px;
  cursor: pointer;
  color: black;
  background: #e0e0e0;
  border: none;
  border-radius: 5px;
  transition: background 0.2s;
}

button:hover {
  background: #c0c0c0;
}
button:nth-child(2),
button:nth-child(3),
button:nth-child(4),
button:nth-child(8),
button:nth-child(12) {
  background: #f7b731;
  color: white;
}

button:nth-child(2):hover,
button:nth-child(3):hover,
button:nth-child(4):hover,
button:nth-child(8):hover,
button:nth-child(12):hover {
  background: #e1a424;
}

```
## OUTPUT
<img width="1843" height="989" alt="image" src="https://github.com/user-attachments/assets/5d3f587c-2017-450b-b8de-2b2617a8b197" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
