### **Assignment: Exploring JavaScript Fundamentals and DOM Manipulation** 🌟

---

#### **Objective:**
This assignment aims to test your understanding of JavaScript basics, control structures, and the Document Object Model (DOM). You will demonstrate your skills by creating an interactive webpage that uses variables, data types, operators, control structures, and DOM manipulation.

---

### **Instructions:**

1. **Create a new HTML file** and include an external JavaScript file for your script.  
2. Name your HTML file as `assignment.html` and your JavaScript file as `script.js`.  
3. Follow the tasks below and ensure you structure your code for readability with proper comments.  

---

### **Tasks:**

#### **Part 1: JavaScript Basics**

1. **Variables and Data Types**:
   - Declare variables of different types: string, number, boolean, array, and object.  
   - Use `console.log()` to print their values and types in the browser console.  

   **Example Output**:  
   ```
   Name: John Doe (Type: string)  
   Age: 25 (Type: number)  
   Is student: true (Type: boolean)  
   ```

2. **Operators**:
   - Write a simple calculator function that performs addition, subtraction, multiplication, and division using two numbers provided by the user (use `prompt()` for input).  
   - Use arithmetic and comparison operators to validate user input and display appropriate messages.

   **Example Output**:  
   ```
   Enter the first number: 10  
   Enter the second number: 2  
   Choose an operation (+, -, *, /): *  
   Result: 20
   ```

3. **Functions**:
   - Create a function named `greetUser` that takes a name as a parameter and returns a greeting message. Display the message in an HTML element.  

---

#### **Part 2: JavaScript Control Structures**

4. **If Statements**:
   - Ask the user for their age using `prompt()`. Use an `if` statement to check if they are eligible to vote (age >= 18). Display a message indicating their eligibility in an HTML element.  

5. **Loops**:
   - Write a loop to display numbers from 1 to 10 on the webpage. Use an ordered list (`<ol>`) to present the numbers.  

---

#### **Part 3: Introduction to the DOM**

6. **Creating HTML Structure**:
   - Add the following HTML elements to your webpage:
     - A heading (`<h1>`) with the text **"JavaScript Assignment"**.  
     - A paragraph (`<p>`) with the text **"Learning JavaScript is fun!"**.  
     - A `<div>` with an `id` of `dynamic-content`.  

7. **Selecting and Modifying HTML Elements**:
   - Use JavaScript to:
     - Change the text of the `<h1>` element to **"JavaScript in Action!"**.  
     - Add a new `<p>` inside the `dynamic-content` `<div>` with the text **"This content was added dynamically using JavaScript."**.  

---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Assignment</title>
    <script src="script.js" defer></script> <!-- Link to the external JS file -->
</head>
<body>

    <!-- Part 3: HTML Structure -->
    <h1>JavaScript Assignment</h1>
    <p>Learning JavaScript is fun!</p>
    <div id="dynamic-content"></div>

    <!-- Part 2: Display result from loops -->
    <ol id="number-list"></ol>

</body>
</html>


// Part 1: JavaScript Basics

// 1. Variables and Data Types
let name = "John Doe";
let age = 25;
let isStudent = true;
let numbers = [1, 2, 3, 4];
let person = { name: "John", age: 25, city: "New York" };

// Output values and their types
console.log(`Name: ${name} (Type: ${typeof name})`);
console.log(`Age: ${age} (Type: ${typeof age})`);
console.log(`Is student: ${isStudent} (Type: ${typeof isStudent})`);
console.log(`Numbers: ${numbers} (Type: ${typeof numbers})`);
console.log(`Person object: ${JSON.stringify(person)} (Type: ${typeof person})`);

// 2. Operators (Simple Calculator)
function calculator() {
    let num1 = parseFloat(prompt("Enter the first number:"));
    let num2 = parseFloat(prompt("Enter the second number:"));
    let operation = prompt("Choose an operation (+, -, *, /):");

    let result;
    if (isNaN(num1) || isNaN(num2)) {
        alert("Please enter valid numbers.");
        return;
    }

    switch(operation) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 === 0) {
                alert("Cannot divide by zero.");
                return;
            }
            result = num1 / num2;
            break;
        default:
            alert("Invalid operation.");
            return;
    }
    
    alert(`Result: ${result}`);
}

// 3. Functions (Greeting Function)
function greetUser(name) {
    return `Hello, ${name}! Welcome to the JavaScript world.`;
}

// Display greeting in HTML element
document.getElementById("dynamic-content").innerHTML = greetUser("Alice");

// Part 2: JavaScript Control Structures

// 4. If Statements (Voting Eligibility)
function checkEligibility() {
    let age = prompt("Please enter your age:");
    age = parseInt(age);

    if (age >= 18) {
        alert("You are eligible to vote.");
    } else {
        alert("You are not eligible to vote.");
    }
}

// 5. Loops (Display Numbers from 1 to 10)
function displayNumbers() {
    let numberList = document.getElementById("number-list");
    for (let i = 1; i <= 10; i++) {
        let listItem = document.createElement("li");
        listItem.textContent = i;
        numberList.appendChild(listItem);
    }
}

// Call the functions to execute them
checkEligibility();
displayNumbers();

// Part 3: DOM Manipulation

// 6. Creating HTML Structure - already defined in assignment.html

// 7. Selecting and Modifying HTML Elements
document.querySelector("h1").textContent = "JavaScript in Action!"; // Modify <h1>
let newParagraph = document.createElement("p");
newParagraph.textContent = "This content was added dynamically using JavaScript.";
document.getElementById("dynamic-content").appendChild(newParagraph); // Append new <p> to #dynamic-content


### **Tips for Success:**

- Test your code frequently to catch errors early.  
- Use meaningful variable names and add comments to explain your logic.  
- Have fun and get creative!  

Happy Coding! 💻✨  
