# Ex03 To-Do List using JavaScript
## Date:

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
1)index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="container">
    <h2>To-Do List</h2>

    <div class="input-section">
      <input type="text" id="taskInput" placeholder="Add a task...">
      <button onclick="addTask()">Add</button>
    </div>

    <ul id="taskList">
      <li>1. Experiment - TO-DO_LIST <button class="delete-btn" onclick="deleteTask(this)">X</button></li>
      <li>2. Skill Assessment <button class="delete-btn" onclick="deleteTask(this)">X</button></li>
      <li>3. Poodle Activity <button class="delete-btn" onclick="deleteTask(this)">X</button></li>
    </ul>

    <footer>
      © 2025 Kathi Hasini 212224240074. All Rights Reserved.
    </footer>
  </div>

  <script src="script.js"></script>
</body>
</html>
```
2)style.css

```
body {
  font-family: Arial, sans-serif;
  background: linear-gradient(to right, #7fd7d7, #b3aef5);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.container {
  background: white;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.2);
  width: 350px;
  text-align: center;
}

h2 {
  margin-bottom: 15px;
}

.input-section {
  display: flex;
  margin-bottom: 20px;
}

input {
  flex: 1;
  padding: 10px;
  border: 2px solid #ddd;
  border-radius: 5px;
  outline: none;
}

button {
  background: #28a745;
  color: white;
  border: none;
  padding: 10px 15px;
  margin-left: 5px;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #218838;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  background: #f4f4f4;
  margin: 8px 0;
  padding: 10px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.delete-btn {
  background: #dc3545;
  color: white;
  border: none;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s;
}

.delete-btn:hover {
  background: #c82333;
}

footer {
  margin-top: 15px;
  font-size: 12px;
  color: gray;
}
```
3)script.js

```
function addTask() {
  let input = document.getElementById("taskInput");
  let taskValue = input.value.trim();

  if (taskValue === "") {
    alert("Please enter a task!");
    return;
  }

  let ul = document.getElementById("taskList");
  let li = document.createElement("li");

  li.innerHTML = taskValue + ' <button class="delete-btn" onclick="deleteTask(this)">X</button>';
  ul.appendChild(li);

  input.value = "";
}

function deleteTask(button) {
  button.parentElement.remove();
}
```
## OUTPUT

<img width="1916" height="1198" alt="image" src="https://github.com/user-attachments/assets/3ca8c38f-1cfc-40ba-b0bb-a5d956b6adce" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
