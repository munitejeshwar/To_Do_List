# Ex03 To-Do List using JavaScript
## Date:
## Name-K Muni Tejeshwar
## Ref no-212223040102
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
```<!DOCTYPE html>
<html lang="en">
<head>
    <title>Todo Application</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #ffffff;
            color: #000;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        header, footer {
            text-align: center;
            padding: 10px;
            background-color: #000;
            color: white;
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            font-size: 14px;
        }
        .todo-container {
            max-width: 500px;
            width: 90%;
            margin: 20px auto;
            padding: 20px;
            background-color: #f9f9f9;
            border: 3px solid #000;
            border-radius: 10px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }
        .todo-input {
            width: 100%;
            padding: 12px;
            margin-bottom: 12px;
            border: 3px solid #000;
            border-radius: 6px;
            font-size: 16px;
            background-color: #fff;
            color: #000;
        }
        .todo-list {
            list-style: none;
            padding: 0;
        }
        .todo-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px;
            margin-bottom: 8px;
            background-color: #ffffff;
            border: 2px solid #000;
            border-radius: 6px;
            font-size: 16px;
        }
        .todo-item.completed {
            text-decoration: line-through;
            color: gray;
        }
        .todo-buttons button {
            padding: 6px 12px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 14px;
        }
        .todo-buttons button:first-child {
            background-color: #000;
            color: white;
        }
        .todo-buttons button:last-child {
            background-color: #d32f2f;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>Todo Application</h1>
    </header>

    <div class="todo-container">
        <h2>Your Tasks</h2>
        <input type="text" id="todo-input" class="todo-input" placeholder="Add a new task">
        <ul id="todo-list" class="todo-list"></ul>
    </div>

    <footer>
        <p>&copy; 2025. All rights reserved 212223040102.</p>
    </footer>

    <script>
        const todoInput = document.getElementById('todo-input');
        const todoList = document.getElementById('todo-list');

        function addTodo() {
            const task = todoInput.value.trim();
            if (task === '') return;

            const li = document.createElement('li');
            li.className = 'todo-item';

            const span = document.createElement('span');
            span.textContent = task;

            const buttonsDiv = document.createElement('div');
            buttonsDiv.className = 'todo-buttons';

            const completeBtn = document.createElement('button');
            completeBtn.textContent = 'Complete';
            completeBtn.onclick = () => {
                li.classList.toggle('completed');
            };

            const deleteBtn = document.createElement('button');
            deleteBtn.textContent = 'Delete';
            deleteBtn.onclick = () => {
                todoList.removeChild(li);
            };

            buttonsDiv.appendChild(completeBtn);
            buttonsDiv.appendChild(deleteBtn);

            li.appendChild(span);
            li.appendChild(buttonsDiv);

            todoList.appendChild(li);
            todoInput.value = '';
        }

        todoInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                addTodo();
            }
        });
    </script>
</body>
</html>
```

## OUTPUT
![image](https://github.com/user-attachments/assets/1cf03242-8079-4766-9de3-325214f8ff81)


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
