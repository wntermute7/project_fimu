# project_fimu
Fiction Multiverse Database
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Simple Website</title>
    <style>
        /* Basic styling for the header and tabs */
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
        .tabs {
            display: flex;
            justify-content: center;
            background-color: #f4f4f4;
            padding: 1rem;
        }
        .tab {
            margin: 0 1rem;
            cursor: pointer;
        }
        .tab.active {
            font-weight: bold;
        }
        .content {
            padding: 1rem;
        }
        /* Styling for the images and information */
        .tab-content {
            display: none;
        }
        .tab-content.active {
            display: block;
        }
        .tab-content img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <header>
        <h1>My Simple Website</h1>
        <div class="tabs">
            <div class="tab active" onclick="showTab('home')">Home</div>
            <div class="tab" onclick="showTab('about')">About</div>
            <div class="tab" onclick="showTab('contact')">Contact</div>
        </div>
    </header>
    <div class="content">
        <div class="tab-content" id="home">
            <h2>Welcome to our website!</h2>
            <p>This is the home page. Feel free to explore.</p>
        </div>
        <div class="tab-content" id="about">
            <h2>About Us</h2>
            <p>We are a team of passionate developers.</p>
        </div>
        <div class="tab-content" id="contact">
            <h2>Contact Us</h2>
            <p>You can reach us at contact@example.com.</p>
        </div>
    </div>
    <script>
        // Function to show the selected tab content
        function showTab(tabId) {
            const tabs = document.querySelectorAll('.tab');
            const tabContents = document.querySelectorAll('.tab-content');
            tabs.forEach(tab => tab.classList.remove('active'));
            tabContents.forEach(content => content.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            document.querySelector(`[onclick="showTab('${tabId}')"]`).classList.add('active');
        }
        // Show the home tab by default
        showTab('home');
    </script>
</body>
</html>
