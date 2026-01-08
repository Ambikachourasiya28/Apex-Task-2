# Apex-Task-2
Great 👍
Below is a **complete, proper solution for Task 2 of your ApexPlanet Internship**, exactly matching the image requirements, with **full source code + step-by-step process**.

---

# ✅ ApexPlanet Internship – Task 2

## **Intermediate HTML, CSS, and JavaScript**

This task includes:

1. Contact Form (HTML + CSS)
2. JavaScript Form Validation
3. Responsive Layout (Flexbox + Grid)
4. Dynamic To-Do List (JavaScript DOM)

---

## 📁 Project Folder Structure

Create a folder like this:

```
task2-apexplanet/
│
├── index.html
├── style.css
└── script.js
```

---

## 🧩 Step 1: Create `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ApexPlanet Task 2</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation -->
    <nav class="navbar">
        <h2>ApexPlanet</h2>
        <ul>
            <li><a href="#contact">Contact</a></li>
            <li><a href="#todo">To-Do</a></li>
        </ul>
    </nav>

    <!-- Main Layout -->
    <div class="container">

        <!-- Contact Form -->
        <section id="contact" class="card">
            <h3>Contact Form</h3>
            <form id="contactForm">
                <input type="text" id="name" placeholder="Enter your name">
                <input type="email" id="email" placeholder="Enter your email">
                <button type="submit">Submit</button>
                <p id="error"></p>
            </form>
        </section>

        <!-- To-Do List -->
        <section id="todo" class="card">
            <h3>To-Do List</h3>
            <input type="text" id="taskInput" placeholder="Enter task">
            <button onclick="addTask()">Add Task</button>
            <ul id="taskList"></ul>
        </section>

    </div>

    <script src="script.js"></script>
</body>
</html>
```

---

## 🎨 Step 2: Create `style.css`

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

/* Navigation using Flexbox */
.navbar {
    display: flex;
    justify-content: space-between;
    padding: 15px;
    background-color: teal;
    color: white;
}

.navbar ul {
    list-style: none;
    display: flex;
}

.navbar ul li {
    margin-left: 15px;
}

.navbar a {
    color: white;
    text-decoration: none;
}

/* Main Container using Grid */
.container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    padding: 20px;
}

/* Card Design */
.card {
    padding: 20px;
    border-radius: 8px;
    background-color: #f4f4f4;
}

/* Form Styling */
input {
    width: 100%;
    padding: 10px;
    margin: 8px 0;
}

button {
    padding: 10px;
    width: 100%;
    background-color: teal;
    color: white;
    border: none;
    cursor: pointer;
}

#error {
    color: red;
    margin-top: 5px;
}

/* Responsive Design */
@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
    }
}
```

---

## 🧠 Step 3: Create `script.js`

```javascript
// Form Validation
document.getElementById("contactForm").addEventListener("submit", function (e) {
    e.preventDefault();

    let name = document.getElementById("name").value;
    let email = document.getElementById("email").value;
    let error = document.getElementById("error");

    if (name === "" || email === "") {
        error.textContent = "All fields are required!";
        return;
    }

    if (!email.includes("@")) {
        error.textContent = "Enter a valid email!";
        return;
    }

    error.textContent = "Form submitted successfully!";
    error.style.color = "green";
});

// To-Do List
function addTask() {
    let taskInput = document.getElementById("taskInput");
    let taskList = document.getElementById("taskList");

    if (taskInput.value === "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");
    li.textContent = taskInput.value;

    li.onclick = function () {
        taskList.removeChild(li);
    };

    taskList.appendChild(li);
    taskInput.value = "";
}
```

---

## 🔄 Full Working Process (Explain in Internship Submission)

### 🔹 1. HTML

* Created contact form using input fields
* Added To-Do list structure
* Linked CSS and JavaScript

### 🔹 2. CSS

* Used **Flexbox** for navigation bar
* Used **CSS Grid** for page layout
* Applied **media queries** for responsiveness

### 🔹 3. JavaScript

* Validated form fields (required + email format)
* Used **DOM manipulation**
* Created dynamic add/remove tasks feature

---

## 📸 Output Features

✔ Responsive webpage
✔ Form validation using JavaScript
✔ Dynamic To-Do list
✔ Clean UI with Flexbox & Grid

---

## ✅ How to Submit

1. Zip the folder `task2-apexplanet`
2. Add screenshots of output
3. Explain steps briefly (use the process section above)

---

If you want:

* 📄 **PDF report**
* ✍️ **Internship explanation in simple words**
* 🎨 **Image gallery instead of To-Do list**

Just tell me 👍
