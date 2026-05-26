# Ex04 Simple Calculator - React Project
## Date: 26-05-2026
## Name: Tarunika D
## register no: 212223040227

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
app.jsx
```
import { useState } from "react";
import "./App.css";

function App() {
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    setResult(result + value);
  };

  const clearResult = () => {
    setResult("");
  };

  const deleteLast = () => {
    setResult(result.slice(0, -1));
  };

  const calculate = () => {
    try {
      setResult(eval(result).toString());
    } catch {
      setResult("Error");
    }
  };

  return (
    <div className="container">
      <div className="calculator">
        <h1>Smart Calculator</h1>

        <input type="text" value={result} readOnly />

        <div className="buttons">
          <button className="special" onClick={clearResult}>
            AC
          </button>

          <button className="special" onClick={deleteLast}>
            DEL
          </button>

          <button className="operator" onClick={() => handleClick("/")}>
            ÷
          </button>

          <button className="operator" onClick={() => handleClick("*")}>
            ×
          </button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button className="operator" onClick={() => handleClick("-")}>
            −
          </button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button className="operator" onClick={() => handleClick("+")}>
            +
          </button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button className="equal" onClick={calculate}>
            =
          </button>

          <button className="zero" onClick={() => handleClick("0")}>
            0
          </button>

          <button onClick={() => handleClick(".")}>.</button>
        </div>
      </div>
    </div>
  );
}

export default App;
```
app.css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

body {
  height: 100vh;
  background: linear-gradient(135deg, #141e30, #243b55);
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.calculator {
  width: 360px;
  padding: 25px;
  border-radius: 25px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(15px);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

.calculator h1 {
  text-align: center;
  color: white;
  margin-bottom: 20px;
}

.calculator input {
  width: 100%;
  height: 70px;
  border: none;
  border-radius: 15px;
  margin-bottom: 20px;
  padding: 15px;
  font-size: 30px;
  text-align: right;
  background: rgba(255, 255, 255, 0.2);
  color: white;
  outline: none;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
}

.buttons button {
  height: 65px;
  border: none;
  border-radius: 15px;
  font-size: 22px;
  cursor: pointer;
  background: rgba(255, 255, 255, 0.15);
  color: white;
}

.operator {
  background: orange;
}

.equal {
  background: green;
}

.special {
  background: crimson;
}

.zero {
  grid-column: span 2;
}
```

## OUTPUT
<img width="1359" height="589" alt="image" src="https://github.com/user-attachments/assets/cce926c6-bba6-4af7-9c42-3c46fc913813" />
<img width="585" height="579" alt="image" src="https://github.com/user-attachments/assets/8ec30400-4d3e-4107-97b7-fac2c55501c1" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
