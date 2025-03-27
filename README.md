# Ex03 To-Do List using JavaScript
## Date:
## Name-K VIJAY
## Ref no-212223040236
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
```
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Todo Application</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: #f4f4f4;
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        header, footer {
            text-align: center;
            padding: 15px;
            background-color: #007acc;
            color: white;
            border-radius: 10px;
            width: 80%;
            max-width: 600px;
            font-size: 16px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .todo-container {
            max-width: 600px;
            width: 80%;
            margin: 20px auto;
            padding: 25px;
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }
        .todo-input {
            width: 100%;
            padding: 14px;
            margin-bottom: 15px;
            border: 2px solid #007acc;
            border-radius: 6px;
            font-size: 18px;
            background-color: #f9f9f9;
            color: #333;
        }
        .todo-list {
            list-style: none;
            padding: 0;
        }
        .todo-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 14px;
            margin-bottom: 10px;
            background-color: #e3f2fd;
            border: 2px solid #007acc;
            border-radius: 8px;
            font-size: 18px;
        }
        .todo-item.completed {
            text-decoration: line-through;
            color: gray;
        }
        .todo-buttons button {
            padding: 8px 14px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 14px;
            transition: background 0.3s;
        }
        .todo-buttons button:first-child {
            background-color: #28a745;
            color: white;
        }
        .todo-buttons button:first-child:hover {
            background-color: #218838;
        }
        .todo-buttons button:last-child {
            background-color: #dc3545;
            color: white;
        }
        .todo-buttons button:last-child:hover {
            background-color: #c82333;
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
        <p>&copy; 2025. All rights reserved by 212223040236.</p>
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
![WhatsApp Image 2025-03-27 at 22 21 24_477d5dba](https://github.com/user-attachments/assets/db2e3024-a56c-4670-8f6d-7fc974823a34)


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
