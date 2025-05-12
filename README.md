# CSS Layouts and Responsive Design

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }

        nav {
            background-color: #333;
            color: white;
            padding: 1em;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: space-around;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            padding: 0.5em 1em;
        }

        /* Main Content (Flexbox Layout) */
        .container {
            display: flex;
            padding: 20px;
            gap: 20px; 
            max-width: 1200px;
            margin: 20px auto;
        }

        .sidebar {
            background-color: #ddd;
            padding: 20px;
            flex: 0 1 300px; 
        }

        .main-content {
            background-color: white;
            padding: 20px;
            flex: 1; 
        }

        .content-item {
            background-color: #eee;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 5px;
        }

        /* Footer (Grid Layout) */
        footer {
            background-color: #333;
            color: white;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            text-align: center;
        }

        footer div {
            padding: 10px;
        }


        @media (max-width: 600px) {
            nav ul {
                flex-direction: column; 
                align-items: center; 
            }

            nav ul li {
                margin-bottom: 0.5em;
            }

            .container {
                flex-direction: column;
            }

            .sidebar {
                width: 100%; 
                margin-bottom: 20px;
            }
        }

        @media (min-width: 601px) and (max-width: 960px) {
            .container {
                flex-direction: row; 
            }

            .sidebar {
                flex: 0 1 200px; 
            }
        }
    </style>
</head>
<body>

    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <div class="container">
        <aside class="sidebar">
            <h3>Sidebar</h3>
            <ul>
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
            </ul>
        </aside>

        <main class="main-content">
            <h2>Main Content</h2>
            <div class="content-item">
                <h3>Section 1</h3>
                <p>This is the content for section 1. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
            <div class="content-item">
                <h3>Section 2</h3>
                <p>This is the content for section 2. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
            </div>
            <div class="content-item">
                <h3>Section 3</h3>
                <p>This is the content for section 3. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            </div>
        </main>
    </div>

    <footer>
        <div>
            <h4>Contact Us</h4>
            <p>Email: info@example.com</p>
            <p>Phone: +1 123-456-7890</p>
        </div>
        <div>
            <h4>Quick Links</h4>
            <ul>
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Terms of Service</a></li>
            </ul>
        </div>
        <div>
            <h4>Follow Us</h4>
            <ul>
                <li><a href="#">Facebook</a></li>
                <li><a href="#">Twitter</a></li>
                <li><a href="#">Instagram</a></li>
            </ul>
        </div>
        <div>
            <p>&copy; 2025 My Website</p>
        </div>
    </footer>

</body>
</html>
