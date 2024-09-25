<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Personal website with Research and CV tabs">
    <title>Your Name - Research & CV</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: white;
            padding: 1rem;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #444;
        }
        nav a {
            color: white;
            padding: 14px 20px;
            text-decoration: none;
            text-align: center;
        }
        nav a:hover {
            background-color: #555;
        }
        .tab-content {
            padding: 2rem;
            display: none;
        }
        .active {
            display: block;
        }
    </style>
</head>
<body>

<header>
    <h1>Your Name</h1>
    <p>Welcome to my personal website</p>
</header>

<nav>
    <a href="#home" onclick="openTab(event, 'home')">Home</a>
    <a href="#research" onclick="openTab(event, 'research')">Research</a>
    <a href="#cv" onclick="openTab(event, 'cv')">CV</a>
</nav>

<div id="home" class="tab-content active">
    <h2>Welcome</h2>
    <p>This is the home page. Introduce yourself and share some general information here.</p>
</div>

<div id="research" class="tab-content">
    <h2>Research</h2>
    <p>Details about your research go here. You can add links to your publications, describe your work, and more.</p>
</div>

<div id="cv" class="tab-content">
    <h2>Curriculum Vitae</h2>
    <p>This is where your CV will go. You can embed a downloadable PDF or write out your experience here.</p>
</div>

<script>
    function openTab(evt, tabName) {
        var i, tabcontent, navlinks;
        tabcontent = document.getElementsByClassName("tab-content");
        for (i = 0; i < tabcontent.length; i++) {
            tabcontent[i].style.display = "none";
        }
        navlinks = document.getElementsByTagName("a");
        for (i = 0; i < navlinks.length; i++) {
            navlinks[i].className = navlinks[i].className.replace(" active", "");
        }
        document.getElementById(tabName).style.display = "block";
        evt.currentTarget.className += " active";
    }

    // Display the home tab by default on page load
    document.getElementById("home").style.display = "block";
</script>

</body>
</html>
