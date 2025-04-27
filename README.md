# Ex03 To-Do List using JavaScript
## Date:28.03.2025

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

# Index.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>To-Do App</title>
  <link rel="stylesheet" href="index.css">
</head>
<body>
  <div class="todo-container">
    <h1> My To-Do List</h1>
    <div class="input-section">
      <input type="text" id="taskInput" placeholder="Enter a new task">
      <button onclick="addTask()">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>

  <script src="index.js"></script>
</body>
</html>

```
# Index.js
````
function addTask() {
    const input = document.getElementById("taskInput");
    const taskText = input.value.trim();
    if (taskText === "") return;
  
    const li = document.createElement("li");
    li.innerHTML = `
      <span onclick="toggleComplete(this)">${taskText}</span>
      <button onclick="deleteTask(this)">Delete</button>
    `;
    document.getElementById("taskList").appendChild(li);
    input.value = "";
  }
  
  function deleteTask(button) {
    button.parentElement.remove();
  }
  
  function toggleComplete(span) {
    span.parentElement.classList.toggle("completed");
  }
  

````
# Index.css
```

body {
    font-family: 'Segoe UI', sans-serif;
    background: #f2f2f2;
    display: flex;
    justify-content: center;
    padding-top: 60px;
  }
  
  .todo-container {
    background: #fff;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(0,0,0,0.1);
    width: 90%;
    max-width: 400px;
  }
  
  h1 {
    text-align: center;
    margin-bottom: 20px;
  }
  
  .input-section {
    display: flex;
    gap: 10px;
  }
  
  input[type="text"] {
    flex: 1;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
  
  button {
    padding: 10px 15px;
    border: none;
    background: #28a745;
    color: white;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button:hover {
    background: #218838;
  }
  
  ul {
    margin-top: 20px;
    list-style: none;
    padding: 0;
  }
  
  li {
    background: #f9f9f9;
    padding: 10px;
    border: 1px solid #ddd;
    margin-bottom: 10px;
    border-radius: 5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  li.completed {
    text-decoration: line-through;
    color: #777;
  }
  
  li button {
    background: #dc3545;
    border: none;
    color: white;
    padding: 5px 10px;
    border-radius: 3px;
    cursor: pointer;
  }
  
  li button:hover {
    background: #c82333;
  }
  

```

## OUTPUT

![image](https://github.com/user-attachments/assets/03f1fbbd-1732-4927-8d03-57fa58f76d33)


![image](https://github.com/user-attachments/assets/8aa2895f-0e20-4a87-9584-7f64d0085a4a)


![image](https://github.com/user-attachments/assets/8b02e092-15aa-4257-adfd-c37767271dc6)

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
