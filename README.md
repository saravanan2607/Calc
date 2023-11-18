# Ex.08 Design of a Standard Calculator
## Date: 04/11/23

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
<html>
<head>
    <title>Simple Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        #calculator-container {
            background-color: #db1111;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(140, 209, 228, 0.2);
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            color: rgb(102, 197, 229); 
        }

        table {
            margin-top: 10px;
        }

        button {
            padding: 10px 20px;
            font-size: 20px;
        }

        /* Define colors for operators */
        button[data-operator="+"] {
            background-color: #bf2424;
        }

        button[data-operator="-"] {
            background-color: #6e0444;
        }

        button[data-operator="*"] {
            background-color: #3b0133;
        }

        button[data-operator="/"] {
            background-color: #52df0c;
        }

        button[data-operator="%"] {
            background-color: #d9bde3;
        }

        button[data-operator="sqrt"] {
            background-color: #daffa6;
        }
    </style>
</head>
<body>
    <div id="calculator-container">
        <h1>Calculator</h1>
        <input type="text" id="display" readonly>
        <table>
            <tr>
                <td><button onclick="appendToDisplay('1')">1</button></td>
                <td><button onclick="appendToDisplay('2')">2</button></td>
                <td><button onclick="appendToDisplay('3')">3</button></td>
                <td><button data-operator="+" onclick="appendToDisplay('+')" style="color: white;">+</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('4')">4</button></td>
                <td><button onclick="appendToDisplay('5')">5</button></td>
                <td><button onclick="appendToDisplay('6')">6</button></td>
                <td><button data-operator="-" onclick="appendToDisplay('-')" style="color: white;">-</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('7')">7</button></td>
                <td><button onclick="appendToDisplay('8')">8</button></td>
                <td><button onclick="appendToDisplay('9')">9</button></td>
                <td><button data-operator="*" onclick="appendToDisplay('*')" style="color: white;">*</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('0')">0</button></td>
                <td><button data-operator="%" onclick="appendToDisplay('%')">%</button></td>
                <td><button data-operator="sqrt" onclick="calculateSquareRoot()">√</button></td>
                <td><button data-operator="/" onclick="appendToDisplay('/')" style="color: white;">/</button></td>
            </tr>
            <tr>
                <td colspan="3"><button onclick="clearDisplay()">C</button></td>
                <td><button onclick="calculateResult()">=</button></td>
            </tr>
        </table>
    </div>
    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculateResult() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }

        function calculateSquareRoot() {
            const inputValue = document.getElementById('display').value;
            const result = Math.sqrt(parseFloat(inputValue));
            document.getElementById('display').value = result;
        }
    </script>
</body>
</html>

## OUTPUT:
![279332204-b5603fa3-c3e7-499f-9861-39f9d746bd60](https://github.com/kamalesh2509/Calc/assets/120444689/b8aef862-8ac6-495d-a05d-86ac73af7a08)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
