<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>LearnHub - Online Learning Platform</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #f4f7fb;
    color: #222;
}

/* HEADER */

header {
    background: #2563eb;
    color: white;
    padding: 15px 6%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo {
    font-size: 25px;
    font-weight: bold;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 8px;
    cursor: pointer;
}

nav a:hover {
    text-decoration: underline;
}

/* HERO */

.hero {
    background: linear-gradient(135deg, #2563eb, #7c3aed);
    color: white;
    text-align: center;
    padding: 80px 20px;
}

.hero h1 {
    font-size: 45px;
    margin-bottom: 15px;
}

.hero p {
    font-size: 19px;
    margin-bottom: 25px;
}

.hero a {
    background: white;
    color: #2563eb;
    padding: 12px 25px;
    text-decoration: none;
    border-radius: 6px;
    font-weight: bold;
}

/* SECTIONS */

.section {
    padding: 50px 6%;
}

.section h2 {
    text-align: center;
    margin-bottom: 30px;
}

/* SEARCH */

.search-box {
    max-width: 600px;
    margin: auto auto 30px;
    display: flex;
}

.search-box input {
    flex: 1;
    padding: 13px;
    border: 1px solid #ccc;
    border-radius: 6px 0 0 6px;
}

.search-box button {
    padding: 13px 20px;
    background: #2563eb;
    color: white;
    border: none;
    border-radius: 0 6px 6px 0;
}

/* COURSES */

.course-container {
    display: grid;
    grid-template-columns:
        repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
}

.course-card {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}

.course-image {
    height: 150px;
    background: #dbeafe;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 55px;
}

.course-content {
    padding: 20px;
}

.course-content h3 {
    margin-bottom: 10px;
}

.course-content p {
    color: #666;
    margin-bottom: 18px;
}

.course-content a {
    display: inline-block;
    width: 100%;
    text-align: center;
    background: #2563eb;
    color: white;
    padding: 11px;
    text-decoration: none;
    border-radius: 6px;
}

.course-content a:hover {
    background: #1d4ed8;
}

/* COURSE READER */

.course-reader {
    display: none;
    background: white;
    padding: 30px;
    margin: 30px auto;
    max-width: 1000px;
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}

.course-reader h2 {
    color: #2563eb;
    margin-bottom: 15px;
}

.course-reader h3 {
    margin-top: 25px;
    margin-bottom: 10px;
}

.course-reader p {
    line-height: 1.7;
    margin-bottom: 15px;
}

.course-reader ul {
    margin-left: 25px;
    line-height: 1.8;
}

.lesson-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin: 20px 0;
}

.lesson-buttons a {
    text-decoration: none;
    background: #e5e7eb;
    color: #111;
    padding: 10px 15px;
    border-radius: 6px;
}

.lesson-buttons a:hover {
    background: #2563eb;
    color: white;
}

.back-link {
    display: inline-block;
    margin-top: 20px;
    background: #111827;
    color: white;
    padding: 10px 18px;
    text-decoration: none;
    border-radius: 6px;
}

/* PROGRESS */

.progress-box {
    background: white;
    padding: 25px;
    border-radius: 10px;
    margin-top: 20px;
}

.progress-bar {
    width: 100%;
    height: 18px;
    background: #ddd;
    border-radius: 20px;
    overflow: hidden;
    margin-top: 10px;
}

.progress-fill {
    height: 100%;
    width: 0%;
    background: #2563eb;
}

/* DASHBOARD */

.stats {
    display: grid;
    grid-template-columns:
        repeat(auto-fit, minmax(180px, 1fr));
    gap: 20px;
}

.stat {
    background: white;
    padding: 25px;
    text-align: center;
    border-radius: 10px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.08);
}

.stat h3 {
    color: #2563eb;
    font-size: 30px;
}

/* QUIZ */

.quiz {
    max-width: 750px;
    margin: auto;
}

.question {
    background: white;
    padding: 20px;
    margin: 15px 0;
    border-radius: 8px;
}

.question label {
    display: block;
    padding: 8px;
}

.quiz button {
    background: #2563eb;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 6px;
}

#quizResult {
    margin-top: 20px;
    font-size: 20px;
    font-weight: bold;
}

/* LOGIN */

.login-box {
    max-width: 450px;
    margin: auto;
    background: white;
    padding: 30px;
    border-radius: 10px;
}

.login-box input {
    width: 100%;
    padding: 12px;
    margin: 8px 0;
    border: 1px solid #ccc;
    border-radius: 6px;
}

.login-box button {
    width: 100%;
    padding: 12px;
    background: #2563eb;
    color: white;
    border: none;
    border-radius: 6px;
    margin-top: 10px;
}

/* FOOTER */

footer {
    background: #111827;
    color: white;
    text-align: center;
    padding: 25px;
    margin-top: 40px;
}

/* MOBILE */

@media(max-width: 700px) {

    header {
        flex-direction: column;
        gap: 15px;
    }

    .hero h1 {
        font-size: 32px;
    }

    nav a {
        font-size: 14px;
    }
}
</style>
</head>

<body>

<!-- ================= HEADER ================= -->

<header>

    <div class="logo">
        📚 LearnHub
    </div>

    <nav>

        <a href="#home">Home</a>

        <a href="#courses">Courses</a>

        <a href="#dashboard">Dashboard</a>

        <a href="#quiz">Quiz</a>

        <a href="#login">Login</a>

    </nav>

</header>


<!-- ================= HOME ================= -->

<section class="hero" id="home">

    <h1>Learn Anything, Anytime</h1>

    <p>
        Learn programming and technology
        through easy lessons.
    </p>

    <a href="#courses">
        Explore Courses
    </a>

</section>


<!-- ================= COURSES ================= -->

<section class="section" id="courses">

    <h2>📚 Available Courses</h2>

    <div class="search-box">

        <input
            type="text"
            id="search"
            placeholder="Search courses..."
            onkeyup="searchCourses()">

        <button onclick="searchCourses()">
            Search
        </button>

    </div>


    <div class="course-container" id="courseList">


        <!-- PYTHON -->

        <div class="course-card"
             data-name="python programming">

            <div class="course-image">
                🐍
            </div>

            <div class="course-content">

                <h3>Python Programming</h3>

                <p>
                    Learn Python from basic
                    to advanced concepts.
                </p>

                <a href="#python"
                   onclick="openCourse('python')">
                    📖 Learn Now
                </a>

            </div>

        </div>


        <!-- WEB DEVELOPMENT -->

        <div class="course-card"
             data-name="web development">

            <div class="course-image">
                🌐
            </div>

            <div class="course-content">

                <h3>Web Development</h3>

                <p>
                    Learn HTML, CSS and
                    JavaScript.
                </p>

                <a href="#web"
                   onclick="openCourse('web')">
                    📖 Learn Now
                </a>

            </div>

        </div>


        <!-- JAVA -->

        <div class="course-card"
             data-name="java programming">

            <div class="course-image">
                ☕
            </div>

            <div class="course-content">

                <h3>Java Programming</h3>

                <p>
                    Learn Java programming
                    step by step.
                </p>

                <a href="#java"
                   onclick="openCourse('java')">
                    📖 Learn Now
                </a>

            </div>

        </div>


        <!-- DATA STRUCTURES -->

        <div class="course-card"
             data-name="data structures">

            <div class="course-image">
                🧩
            </div>

            <div class="course-content">

                <h3>Data Structures</h3>

                <p>
                    Learn arrays, stacks,
                    queues and trees.
                </p>

                <a href="#dsa"
                   onclick="openCourse('dsa')">
                    📖 Learn Now
                </a>

            </div>

        </div>


        <!-- AI -->

        <div class="course-card"
             data-name="artificial intelligence">

            <div class="course-image">
                🤖
            </div>

            <div class="course-content">

                <h3>Artificial Intelligence</h3>

                <p>
                    Learn basic AI concepts
                    and algorithms.
                </p>

                <a href="#ai"
                   onclick="openCourse('ai')">
                    📖 Learn Now
                </a>

            </div>

        </div>


        <!-- MACHINE LEARNING -->

        <div class="course-card"
             data-name="machine learning">

            <div class="course-image">
                🧠
            </div>

            <div class="course-content">

                <h3>Machine Learning</h3>

                <p>
                    Learn machine learning
                    fundamentals.
                </p>

                <a href="#ml"
                   onclick="openCourse('ml')">
                    📖 Learn Now
                </a>

            </div>

        </div>

    </div>

</section>


<!-- ================= COURSE READER ================= -->

<section class="course-reader"
         id="courseReader">

    <h2 id="readerTitle">
        Course
    </h2>

    <div class="lesson-buttons">

        <a href="#lesson1"
           onclick="showLesson(1)">
            Lesson 1
        </a>

        <a href="#lesson2"
           onclick="showLesson(2)">
            Lesson 2
        </a>

        <a href="#lesson3"
           onclick="showLesson(3)">
            Lesson 3
        </a>

        <a href="#lesson4"
           onclick="showLesson(4)">
            Lesson 4
        </a>

        <a href="#lesson5"
           onclick="showLesson(5)">
            Lesson 5
        </a>

    </div>


    <article id="readingContent">

        <h3>Welcome to the Course</h3>

        <p>
            Select a lesson above to start learning.
        </p>

    </article>


    <br>

    <a href="#courses"
       class="back-link"
       onclick="closeCourse()">
        ← Back to Courses
    </a>

</section>


<!-- ================= DASHBOARD ================= -->

<section class="section" id="dashboard">

    <h2>📊 Student Dashboard</h2>

    <div class="progress-box">

        <h3>
            Welcome,
            <span id="studentName">
                Student
            </span>
        </h3>

        <p>
            Track your learning progress.
        </p>

        <div class="progress-bar">

            <div
                class="progress-fill"
                id="progressFill">
            </div>

        </div>

        <p id="progressText">
            0% completed
        </p>

    </div>


    <div class="stats">

        <div class="stat">

            <h3 id="completedLessons">
                0
            </h3>

            <p>
                Lessons Completed
            </p>

        </div>


        <div class="stat">

            <h3>
                6
            </h3>

            <p>
                Available Courses
            </p>

        </div>


        <div class="stat">

            <h3 id="quizScore">
                0%
            </h3>

            <p>
                Quiz Score
            </p>

        </div>

    </div>

</section>


<!-- ================= QUIZ ================= -->

<section class="section" id="quiz">

    <h2>📝 Programming Quiz</h2>

    <div class="quiz">

        <div class="question">

            <h3>
                1. Which language is used
                to create web pages?
            </h3>

            <label>
                <input type="radio"
                       name="q1"
                       value="HTML">
                HTML
            </label>

            <label>
                <input type="radio"
                       name="q1"
                       value="Python">
                Python
            </label>

            <label>
                <input type="radio"
                       name="q1"
                       value="Java">
                Java
            </label>

        </div>


        <div class="question">

            <h3>
                2. Which language is used
                for web page styling?
            </h3>

            <label>
                <input type="radio"
                       name="q2"
                       value="CSS">
                CSS
            </label>

            <label>
                <input type="radio"
                       name="q2"
                       value="Java">
                Java
            </label>

            <label>
                <input type="radio"
                       name="q2"
                       value="Python">
                Python
            </label>

        </div>


        <div class="question">

            <h3>
                3. Which language adds
                interactivity to websites?
            </h3>

            <label>
                <input type="radio"
                       name="q3"
                       value="JavaScript">
                JavaScript
            </label>

            <label>
                <input type="radio"
                       name="q3"
                       value="HTML">
                HTML
            </label>

            <label>
                <input type="radio"
                       name="q3"
                       value="CSS">
                CSS
            </label>

        </div>


        <button onclick="submitQuiz()">
            Submit Quiz
        </button>

        <div id="quizResult"></div>

    </div>

</section>


<!-- ================= LOGIN ================= -->

<section class="section" id="login">

    <h2>👤 Student Login</h2>

    <div class="login-box">

        <input
            type="text"
            id="name"
            placeholder="Enter your name">

        <input
            type="email"
            id="email"
            placeholder="Enter email">

        <input
            type="password"
            id="password"
            placeholder="Enter password">

        <button onclick="login()">
            Login
        </button>

        <p id="loginMessage"></p>

    </div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

    <p>
        © 2026 LearnHub Online Learning Platform
    </p>

</footer>


<script>

/* ==============================
   COURSE CONTENT
============================== */

const courseData = {

    python: {

        title: "🐍 Python Programming",

        lessons: [

            {
                title: "Introduction to Python",

                content: `
                <h3>Introduction to Python</h3>

                <p>
                Python is a high-level,
                interpreted programming language.
                It is easy to learn and widely
                used in software development.
                </p>

                <h3>Uses of Python</h3>

                <ul>
                    <li>Web Development</li>
                    <li>Artificial Intelligence</li>
                    <li>Machine Learning</li>
                    <li>Data Science</li>
                    <li>Automation</li>
                </ul>
                `
            },

            {
                title: "Variables",

                content: `
                <h3>Python Variables</h3>

                <p>
                A variable is used to store data.
                </p>

                <p>
                Example:
                </p>

                <pre>
name = "Harish"
age = 20
                </pre>

                <p>
                Python automatically identifies
                the data type.
                </p>
                `
            },

            {
                title: "If Else",

                content: `
                <h3>If-Else Statement</h3>

                <p>
                If-else statements are used
                for decision making.
                </p>

                <pre>
age = 18

if age >= 18:
    print("Eligible")

else:
    print("Not Eligible")
                </pre>
                `
            },

            {
                title: "Loops",

                content: `
                <h3>Python Loops</h3>

                <p>
                Loops are used to repeat
                a block of code.
                </p>

                <pre>
for i in range(5):
    print(i)
                </pre>
                `
            },

            {
                title: "Functions",

                content: `
                <h3>Python Functions</h3>

                <p>
                A function is a reusable block
                of code.
                </p>

                <pre>
def greet():
    print("Hello")

greet()
                </pre>
                `
            }

        ]

    },


    web: {

        title: "🌐 Web Development",

        lessons: [

            {
                title: "Introduction to HTML",

                content: `
                <h3>Introduction to HTML</h3>

                <p>
                HTML stands for HyperText
                Markup Language.
                </p>

                <p>
                HTML is used to create
                the structure of web pages.
                </p>

                <pre>
&lt;h1&gt;Hello World&lt;/h1&gt;
                </pre>
                `
            },

            {
                title: "HTML Elements",

                content: `
                <h3>HTML Elements</h3>

                <p>
                HTML elements are represented
                using tags.
                </p>

                <pre>
&lt;p&gt;This is a paragraph&lt;/p&gt;
&lt;h1&gt;Heading&lt;/h1&gt;
&lt;a href="#"&gt;Link&lt;/a&gt;
                </pre>
                `
            },

            {
                title: "CSS Basics",

                content: `
                <h3>CSS Basics</h3>

                <p>
                CSS stands for Cascading Style Sheets.
                </p>

                <p>
                CSS is used to design and style
                web pages.
                </p>

                <pre>
body {
    background: lightblue;
}

h1 {
    color: blue;
}
                </pre>
                `
            },

            {
                title: "JavaScript",

                content: `
                <h3>JavaScript</h3>

                <p>
                JavaScript adds interactivity
                to websites.
                </p>

                <pre>
function hello() {
    alert("Hello World");
}
                </pre>
                `
            },

            {
                title: "Build a Website",

                content: `
                <h3>Building a Website</h3>

                <p>
                A basic website normally uses:
                </p>

                <ul>
                    <li>HTML - Structure</li>
                    <li>CSS - Design</li>
                    <li>JavaScript - Interaction</li>
                </ul>
                `
            }

        ]

    },


    java: {

        title: "☕ Java Programming",

        lessons: [

            {
                title: "Introduction to Java",

                content: `
                <h3>Introduction to Java</h3>

                <p>
                Java is an object-oriented
                programming language.
                </p>

                <p>
                Java programs can run on
                different platforms using
                the Java Virtual Machine.
                </p>
                `
            },

            {
                title: "Variables",

                content: `
                <h3>Java Variables</h3>

                <pre>
int age = 20;
double mark = 90.5;
String name = "Student";
                </pre>
                `
            },

            {
                title: "If Else",

                content: `
                <h3>Java If-Else</h3>

                <pre>
int age = 20;

if(age >= 18) {
    System.out.println("Adult");
}
else {
    System.out.println("Minor");
}
                </pre>
                `
            },

            {
                title: "Loops",

                content: `
                <h3>Java Loops</h3>

                <pre>
for(int i=1; i<=5; i++) {
    System.out.println(i);
}
                </pre>
                `
            },

            {
                title: "Classes and Objects",

                content: `
                <h3>Classes and Objects</h3>

                <p>
                A class is a blueprint for creating
                objects.
                </p>

                <pre>
class Student {
    String name;
}

Student s = new Student();
                </pre>
                `
            }

        ]

    },


    dsa: {

        title: "🧩 Data Structures",

        lessons: [

            {
                title: "Arrays",

                content: `
                <h3>Arrays</h3>

                <p>
                An array stores multiple values
                of the same type.
                </p>

                <pre>
int arr[] = {10,20,30,40};
                </pre>
                `
            },

            {
                title: "Linked List",

                content: `
                <h3>Linked List</h3>

                <p>
                A linked list consists of nodes.
                Each node contains data and a
                reference to the next node.
                </p>
                `
            },

            {
                title: "Stack",

                content: `
                <h3>Stack</h3>

                <p>
                Stack follows LIFO:
                Last In First Out.
                </p>

                <p>
                Example: Undo operation.
                </p>
                `
            },

            {
                title: "Queue",

                content: `
                <h3>Queue</h3>

                <p>
                Queue follows FIFO:
                First In First Out.
                </p>

                <p>
                Example: Printer queue.
                </p>
                `
            },

            {
                title: "Trees",

                content: `
                <h3>Tree</h3>

                <p>
                A tree is a non-linear data
                structure consisting of nodes.
                </p>

                <p>
                Binary Search Tree is a common
                type of tree.
                </p>
                `
            }

        ]

    },


    ai: {

        title: "🤖 Artificial Intelligence",

        lessons: [

            {
                title: "Introduction to AI",

                content: `
                <h3>Introduction to AI</h3>

                <p>
                Artificial Intelligence is the
                field of creating systems that
                can perform tasks requiring
                human-like intelligence.
                </p>
                `
            },

            {
                title: "Intelligent Agents",

                content: `
                <h3>Intelligent Agents</h3>

                <p>
                An intelligent agent perceives
                its environment and takes actions.
                </p>
                `
            },

            {
                title: "Search Algorithms",

                content: `
                <h3>Search Algorithms</h3>

                <p>
                Search algorithms help AI systems
                find solutions to problems.
                </p>

                <ul>
                    <li>BFS</li>
                    <li>DFS</li>
                    <li>Uniform Cost Search</li>
                    <li>A* Search</li>
                </ul>
                `
            },

            {
                title: "A* Algorithm",

                content: `
                <h3>A* Algorithm</h3>

                <p>
                A* is a pathfinding and graph
                traversal algorithm.
                </p>

                <p>
                It uses the cost function:
                </p>

                <pre>
f(n) = g(n) + h(n)
                </pre>
                `
            },

            {
                title: "AI Applications",

                content: `
                <h3>Applications of AI</h3>

                <ul>
                    <li>Self-driving vehicles</li>
                    <li>Chatbots</li>
                    <li>Medical diagnosis</li>
                    <li>Robotics</li>
                    <li>Recommendation systems</li>
                </ul>
                `
            }

        ]

    },


    ml: {

        title: "🧠 Machine Learning",

        lessons: [

            {
                title: "Introduction to ML",

                content: `
                <h3>Introduction to Machine Learning</h3>

                <p>
                Machine Learning is a branch of
                AI that allows computers to learn
                from data.
                </p>
                `
            },

            {
                title: "Types of ML",

                content: `
                <h3>Types of Machine Learning</h3>

                <ul>
                    <li>Supervised Learning</li>
                    <li>Unsupervised Learning</li>
                    <li>Reinforcement Learning</li>
                </ul>
                `
            },

            {
                title: "Linear Regression",

                content: `
                <h3>Linear Regression</h3>

                <p>
                Linear regression is used to predict
                a continuous value.
                </p>
                `
            },

            {
                title: "Classification",

                content: `
                <h3>Classification</h3>

                <p>
                Classification is used to predict
                categories or classes.
                </p>

                <p>
                Example:
                Spam or Not Spam.
                </p>
                `
            },

            {
                title: "Model Evaluation",

                content: `
                <h3>Model Evaluation</h3>

                <p>
                Machine learning models can be
                evaluated using metrics such as:
                </p>

                <ul>
                    <li>Accuracy</li>
                    <li>Precision</li>
                    <li>Recall</li>
                    <li>F1 Score</li>
                </ul>
                `
            }

        ]

    }

};


/* ==============================
   OPEN COURSE
============================== */

let selectedCourse = "";
let completed = 0;

function openCourse(course) {

    selectedCourse = course;

    const reader =
        document.getElementById("courseReader");

    reader.style.display = "block";

    document.getElementById("readerTitle")
        .innerText =
        courseData[course].title;

    document.getElementById("readingContent")
        .innerHTML = `
        <h3>
            Welcome to
            ${courseData[course].title}
        </h3>

        <p>
            Select a lesson above to start
            reading and learning.
        </p>
        `;

    reader.scrollIntoView({
        behavior: "smooth"
    });

}


/* ==============================
   SHOW LESSON
============================== */

function showLesson(number) {

    const lesson =
        courseData[selectedCourse]
        .lessons[number - 1];

    document.getElementById("readingContent")
        .innerHTML =
        lesson.content;

    completed++;

    if (completed > 5) {
        completed = 5;
    }

    updateProgress();

}


/* ==============================
   CLOSE COURSE
============================== */

function closeCourse() {

    document.getElementById("courseReader")
        .style.display = "none";

}


/* ==============================
   SEARCH COURSES
============================== */

function searchCourses() {

    const value =
        document.getElementById("search")
        .value
        .toLowerCase();

    const cards =
        document.querySelectorAll(".course-card");

    cards.forEach(card => {

        const name =
            card.getAttribute("data-name");

        if (name.includes(value)) {

            card.style.display = "block";

        } else {

            card.style.display = "none";

        }

    });

}


/* ==============================
   PROGRESS
============================== */

function updateProgress() {

    const percentage =
        completed * 20;

    document.getElementById("progressFill")
        .style.width =
        percentage + "%";

    document.getElementById("progressText")
        .innerText =
        percentage + "% completed";

    document.getElementById("completedLessons")
        .innerText =
        completed;

}


/* ==============================
   LOGIN
============================== */

function login() {

    const name =
        document.getElementById("name")
        .value;

    const email =
        document.getElementById("email")
        .value;

    const password =
        document.getElementById("password")
        .value;

    if (
        name === "" ||
        email === "" ||
        password === ""
    ) {

        document.getElementById("loginMessage")
            .innerText =
            "Please fill all fields.";

        return;

    }

    localStorage.setItem(
        "studentName",
        name
    );

    document.getElementById("studentName")
        .innerText =
        name;

    document.getElementById("loginMessage")
        .innerText =
        "Login successful!";

}


/* ==============================
   QUIZ
============================== */

function submitQuiz() {

    let score = 0;

    const q1 =
        document.querySelector(
            'input[name="q1"]:checked'
        );

    const q2 =
        document.querySelector(
            'input[name="q2"]:checked'
        );

    const q3 =
        document.querySelector(
            'input[name="q3"]:checked'
        );

    if (q1 && q1.value === "HTML") {
        score++;
    }

    if (q2 && q2.value === "CSS") {
        score++;
    }

    if (q3 && q3.value === "JavaScript") {
        score++;
    }

    const percentage =
        Math.round((score / 3) * 100);

    document.getElementById("quizResult")
        .innerText =
        "Your Score: " +
        score +
        "/3 = " +
        percentage +
        "%";

    document.getElementById("quizScore")
        .innerText =
        percentage + "%";

}


/* ==============================
   LOAD SAVED USER
============================== */

window.onload = function() {

    const savedName =
        localStorage.getItem(
            "studentName"
        );

    if (savedName) {

        document.getElementById("studentName")
            .innerText =
            savedName;

    }

};

</script>

</body>
</html>
