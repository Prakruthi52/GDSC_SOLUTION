<!DOCTYPE html>
<html>
<head>
    <title>LifeInLand</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            position: relative;
            color: rgb(0, 0, 0);
            text-align: center;
            font-size: 18px; /* Increase the font size for everything */
            /* Other styles... */
        }
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url(E:\im1.jpg);
            background-size: cover;
            background-position: center;
            opacity: 0.7; /* Set the opacity for the background image */
            z-index: -1;
        }
        .navbar {
            overflow: hidden;
            background-color: #008000fe;
            position: relative;
            animation: slideIn 2s;
            text-align: center;
        }
        @keyframes slideIn {
            from {left: -300px;}
            to {left: 0;}
        }

        .navbar a {
            float: none; /* Remove float property */
            display: inline-block; /* Center-align the navbar links */
            color: #020100;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
            transition: background-color 0.5s ease;
        }
        .navbar a:hover {
            background-color: #45b945;
            color: black;
        }
        h2 {
            color: #124403;
            transition: color 1s;
        }
        h2:hover {
            color: #fefff1;
        }
        .hidden-content {
            text-align: left; /* Align the content inside hidden-content to the left */
            margin: 0 auto; /* Center-align the hidden-content div */
            max-width: 800px; /* Set a maximum width for better readability */
        }
        form {
            margin-top: 20px; /* Add some space above the form */
        }
        .report-input {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
        }
        .report-button {
            padding: 10px;
            background-color: #45b945;
            color: black;
            border: none;
            cursor: pointer;
        }
        .report-button:hover {
            background-color: #020100;
            color: white;
        }
    </style>
</head>
<body>

<div class="navbar">
  <a href="#home" onclick="showContent('home')">Home</a>
  <a href="#GreenWoodMaps" onclick="showContent('greenwood')">GreenWood Maps</a>
  <a href="#rReportIssue" onclick="showContent('report')">Report Issue</a>
  <a href="#ContactOfficials" onclick="showContent('contact')">Contact Officials</a>
  <a href="#Analysis" onclick="showContent('analysis')">Analysis</a>
</div>

<!-- Content for GreenWood Maps -->
<div id="home-content" class="hidden-content">  
    <h2>Welcome to Green Guardians</h2>
    <p>🌿 Welcome to Green Guardians, your ultimate platform for environmental empowerment! Dive into a world of comprehensive geographical data on forests, reserved regions, and biological habitats gathered from dedicated organizations. Connect with forest officials and conservationists effortlessly, ensuring up-to-date insights on our planet's precious ecosystems. Be a guardian against illegal activities by reporting incidents of poaching, trafficking, or deforestation, triggering swift action from authorities. Engage in our vibrant community, fostering collective efforts to address environmental concerns and make a real impact. Stay ahead of emergencies with our weather tracking alerts, safeguarding against forest fires and other calamities. Explore crop data for informed agriculture decisions, promoting sustainable land management and community well-being. Our platform's success will be reflected in a 30% increase in reported incidents, highlighting the transformative role of community involvement. Join us at Green Guardians and embark on a journey where every action contributes to the protection and preservation of our planet's natural wonders. 🌍✨</p>
    <h2>Login Page</h2>
      <form action="/action_page.php">
      <label for="username">Username:</label><br>
      <input type="text" id="username" name="username"><br>
      <label for="password">Password:</label><br>
      <input type="password" id="password" name="password"><br><br>
      <input type="submit" value="Login">
    </form> 
</div>

<div id="greenwood-content" class="hidden-content">
    <h2>GreenWood Maps</h2>
    <p>Welcome to the GreenWood Maps section! Explore detailed data about forest covers, reserved regions, and biological habitats. Navigate through interactive maps to gain insights into the diverse ecosystems our planet holds. Discover the richness of our forests and learn about the importance of preserving these natural wonders. Whether you're an environmental enthusiast or a researcher, GreenWood Maps provides a visual journey into the heart of our planet's green landscapes</p>
</div>

<div id="report-content" class="hidden-content">
    <h2>Report Issue</h2>
    <p>Report environmental concerns and be a guardian of our forests! If you witness any illegal activities such as poaching, trafficking, or deforestation in specific areas, use this platform to raise your voice. Your reports trigger swift action from authorities, contributing to the protection of our ecosystems. Every report matters, and together we can ensure the safety and well-being of our natural habitats. Join us in actively preserving the environment by reporting any suspicious activities you encounter.</p>
    <input type="text" class="report-input" id="reportInput" placeholder="Type your issue here...">
    <button class="report-button" onclick="submitReport()">Submit Report</button>
</div>

<div id="contact-content" class="hidden-content">
    <h2>Contact Officials</h2>
    <p>Connect with the stewards of nature! In the Contact Officials section, you can find the contact details of nearby forest officials and environmental conservationists. Building a bridge between the community and those working on the front lines of conservation, this feature enables you to reach out to experts. Whether you have questions, suggestions, or want to report an urgent matter, this platform facilitates direct communication. Let's collaborate with the dedicated individuals working towards environmental protection.</p>
</div>

<div id="analysis-content" class="hidden-content">
    <h2>Analysis</h2>
    <p>Uncover insights to protect our planet! The Analysis section provides a deeper understanding of environmental patterns, helping predict areas where poaching and other illegal activities may occur. By harnessing data-driven analysis, we empower proactive conservation efforts. Explore the analytics to grasp the dynamics of our ecosystems and contribute to informed decision-making for a sustainable future. Together, let's use knowledge as a tool to safeguard the delicate balance of our environment.</p>
</div>

<script>
    // Show only the login page initially
    document.getElementById('home-content').style.display = 'block';

    function showContent(contentId) {
        // Hide all content
        var allContent = document.getElementsByClassName('hidden-content');
        for (var i = 0; i < allContent.length; i++) {
            allContent[i].style.display = 'none';
        }

        // Show the selected content
        var selectedContent = document.getElementById(contentId + '-content');
        if (selectedContent) {
            selectedContent.style.display = 'block';
        }
    }

    function submitReport() {
        // Retrieve the content of the report input
        var reportContent = document.getElementById('reportInput').value;

        // You can add further logic here to handle the reported issue (e.g., sending it to a server, etc.)

        // For now, just display an alert with the reported issue
        alert('Reported Issue: ' + reportContent);
    }
</script>

</body>
</html>
