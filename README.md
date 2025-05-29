# Ex.07 Restaurant Website
## Date:

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Reservation - Velvet Bistro</title>
        <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto:wght@300;400;500&family=Gloock&display=swap" rel="stylesheet">
        <style>
            body {
                font-family: 'Roboto', sans-serif;
                margin: 0;
                padding: 0;
                background-color: #1a1a1a;
                color: #ddd;
            }

            .header {
                background-color: #111;
                padding: 15px 30px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                color: #fff;
            }

            .header .logo h1 {
                margin: 0;
                font-family: 'Poppins', sans-serif;
                font-size: 26px;
            }

            .header .logo img {
                height: 40px;
                width: auto;
                margin-left: 10px;
            }

            .header .search-bar input {
                padding: 10px;
                width: 350px;
                border-radius: 20px;
                border: 1px solid #444;
                margin-right: 10px;
                font-size: 1em;
                background-color: #333;
                color: white;
            }

            .header .search-bar button {
                padding: 10px 20px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1em;
                color: #fff;
            }

            .nav {
                background-color: #222;
                color: white;
                padding: 15px 0;
            }

            .nav ul {
                display: flex;
                justify-content: center;
                list-style: none;
                margin: 0;
                padding: 0;
            }

            .nav ul li {
                margin: 0 25px;
                cursor: pointer;
            }

            .nav ul li a {
                text-decoration: none;
                color: white;
                font-size: 1.1em;
                transition: color 0.3s;
            }

            .nav ul li a:hover {
                color: #f39c12;
            }

            .reservation-section {
                text-align: center;
                padding: 60px 30px;
                background-color: #111;
                margin: 30px 0;
                border-bottom: 5px solid #f39c12;
            }

            .reservation-section h2 {
                font-family: 'Gloock', sans-serif;
                font-size: 3.5em;
                color: #f39c12;
                margin-bottom: 20px;
                text-transform: uppercase;
            }

            .reservation-section p {
                font-size: 1.1em;
                color: #ccc;
                margin-bottom: 30px;
            }

            .reservation-form {
                background-color: #222;
                padding: 40px;
                border-radius: 10px;
                max-width: 800px;
                margin: 0 auto;
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            }

            .reservation-form input,
            .reservation-form select,
            .reservation-form textarea {
                width: 100%;
                padding: 15px;
                margin-bottom: 20px;
                border: 1px solid #444;
                border-radius: 5px;
                background-color: #333;
                color: white;
                font-size: 1em;
            }

            .reservation-form button {
                padding: 15px 30px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1.1em;
                color: white;
                width: 100%;
            }

            .reservation-form button:hover {
                background-color: #e67e22;
            }

            footer {
                background-color: #111;
                color: white;
                padding: 20px 0;
                text-align: center;
            }

            footer a {
                color: #f39c12;
                text-decoration: none;
                margin: 0 10px;
            }

            footer a:hover {
                text-decoration: underline;
            }
        </style>
    </head>
    <body>
        <header class="header">
            <div class="logo">
                <img src="logo.jpg" alt="logo">
                <h1></h1>
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Search for your favorite dishes...">
                <button>Search</button>
            </div>
        </header>

        <nav class="nav">
            <ul>
                <li><a href="home.html">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="admin.html">Admin</a></li>
                <li><a href="contact.html">Contact Us</a></li>
            </ul>
        </nav>

        <section class="reservation-section">
            <h2>Make a Reservation</h2>
            <p>Reserve a table and experience a dining experience like no other at Velvet Bistro.</p>
            <div class="reservation-form">
                <form action="submit-reservation.php" method="POST">
                    <label for="name">Full Name:</label>
                    <input type="text" id="name" name="name" required>

                    <label for="email">Email Address:</label>
                    <input type="email" id="email" name="email" required>

                    <label for="phone">Phone Number:</label>
                    <input type="text" id="phone" name="phone" required>

                    <label for="date">Reservation Date:</label>
                    <input type="date" id="date" name="date" required>

                    <label for="time">Reservation Time:</label>
                    <input type="time" id="time" name="time" required>

                    <label for="guests">Number of Guests:</label>
                    <select id="guests" name="guests" required>
                        <option value="1">1</option>
                        <option value="2">2</option>
                        <option value="3">3</option>
                        <option value="4">4</option>
                        <option value="5">5</option>
                        <option value="6">6</option>
                        <option value="7">7</option>
                        <option value="8">8</option>
                        <option value="9">9</option>
                        <option value="10">10</option>
                    </select>

                    <label for="special_requests">Special Requests (optional):</label>
                    <textarea id="special_requests" name="special_requests"></textarea>

                    <button type="submit">Submit Reservation</button>
                </form>
            </div>
        </section>

        <footer>
            <p>&copy; 2024 Velvet Bistro | <a href="privacy.html">Privacy Policy</a> | <a href="terms.html">Terms & Conditions</a></p>
        </footer>
    </body>
</html>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Admin Dashboard - Velvet Bistro</title>
        <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto:wght@300;400;500&family=Gloock&display=swap" rel="stylesheet">
        <style>
            body {
                font-family: 'Roboto', sans-serif;
                margin: 0;
                padding: 0;
                background-color: #1a1a1a;
                color: #ddd;
            }

            .header {
                background-color: #111;
                padding: 15px 30px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                color: #fff;
            }

            .header .logo h1 {
                margin: 0;
                font-family: 'Poppins', sans-serif;
                font-size: 26px;
            }

            .header .logo img {
                height: 40px;
                width: auto;
                margin-left: 10px;
            }

            .header .search-bar input {
                padding: 10px;
                width: 350px;
                border-radius: 20px;
                border: 1px solid #444;
                margin-right: 10px;
                font-size: 1em;
                background-color: #333;
                color: white;
            }

            .header .search-bar button {
                padding: 10px 20px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1em;
                color: #fff;
            }

            .nav {
                background-color: #222;
                color: white;
                padding: 15px 0;
            }

            .nav ul {
                display: flex;
                justify-content: center;
                list-style: none;
                margin: 0;
                padding: 0;
            }

            .nav ul li {
                margin: 0 25px;
                cursor: pointer;
            }

            .nav ul li a {
                text-decoration: none;
                color: white;
                font-size: 1.1em;
                transition: color 0.3s;
            }

            .nav ul li a:hover {
                color: #f39c12;
            }

            .admin-dashboard {
                padding: 60px 30px;
                text-align: center;
                background-color: #111;
                margin: 30px 0;
                border-bottom: 5px solid #f39c12;
            }

            .admin-dashboard h2 {
                font-family: 'Gloock', sans-serif;
                font-size: 3.5em;
                color: #f39c12;
                margin-bottom: 20px;
                text-transform: uppercase;
            }

            .admin-dashboard p {
                font-size: 1.1em;
                color: #ccc;
                margin-bottom: 30px;
            }

            .admin-team {
                display: flex;
                justify-content: space-around;
                flex-wrap: wrap;
                margin-top: 40px;
            }

            .admin-card {
                background-color: #222;
                width: 250px;
                margin: 20px;
                padding: 20px;
                text-align: center;
                border-radius: 10px;
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
                transition: transform 0.3s;
            }

            .admin-card:hover {
                transform: translateY(-10px);
            }

            .admin-card img {
                width: 100px;
                height: 100px;
                border-radius: 50%;
                object-fit: cover;
                margin-bottom: 15px;
            }

            .admin-card h3 {
                color: #f39c12;
                font-size: 1.5em;
                margin-bottom: 10px;
            }

            .admin-card p {
                color: #ccc;
                font-size: 1em;
                margin-bottom: 15px;
            }

            .admin-card .position {
                font-size: 1.1em;
                color: #ddd;
            }

            footer {
                background-color: #111;
                color: white;
                padding: 20px 0;
                text-align: center;
            }

            footer a {
                color: #f39c12;
                text-decoration: none;
                margin: 0 10px;
            }

            footer a:hover {
                text-decoration: underline;
            }
        </style>
    </head>
    <body>
        <header class="header">
            <div class="logo">
                <img src="logo.jpg" alt="logo">
                <h1></h1>
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Search for reservations...">
                <button>Search</button>
            </div>
        </header>

        <nav class="nav">
            <ul>
                <li><a href="home.html">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="reservation.html">Make a Reservation</a></li>
                <li><a href="contact.html">Contact Us</a></li>
                <li><a href="admin.html">Admin Dashboard</a></li>
            </ul>
        </nav>

        <section class="admin-dashboard">
            <h2>Admin Dashboard</h2>
            <p>Manage your restaurant's reservations, menu, and staff. Welcome, admin!</p>

            <div class="admin-team">
                <!-- Admin 1 -->
                <div class="admin-card">
                    <h3>iniya</h3>
                    <p class="position">CEO</p>
                    <p>Responsible for overall functioning of the restaurant setting and executing the organization's strategy, allocating capital, and building and overseeing the executive team.</p>
                </div>

                <!-- Admin 2 -->
                <div class="admin-card">
                    <img src=" 1.png">
                    <h3>hema</h3>
                    <p class="position">Chef</p>
                    <p>Head of kitchen operations, ensuring quality control, menu design, and food preparation standards.</p>
                </div>

                <!-- Admin 3 -->
                <div class="admin-card">
                    <img src="2.png" alt="Admin 3">
                    <h3>harsita</h3>
                    <p class="position">Reservation Manager</p>
                    <p>Manages all reservations, coordinates with guests, and ensures smooth seating arrangements.</p>
                </div>

                <!-- Admin 4 -->
                <div class="admin-card">
                    <img src="3.png">
                    <h3>kani</h3>
                    <p class="position">Marketing Manager</p>
                    <p>Handles restaurant promotions, social media presence, and marketing campaigns.</p>
                </div>

                <!-- Admin 5 -->
                <div class="admin-card">
                    <img src="4.jpg">
                    <h3>sri</h3>
                    <p class="position">Operations Manager</p>
                    <p>Responsible for maintaining restaurant operations, supplies, and day-to-day management.</p>
                </div>
            </div>
        </section>

        <footer>
            <p>&copy; 2024 Velvet Bistro | Privacy Policy | Terms & Conditions</p>
        </footer>
    </body>
</html>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Contact Us - Velvet Bistro</title>
        <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto:wght@300;400;500&family=Gloock&display=swap" rel="stylesheet">
        <style>
            body {
                font-family: 'Roboto', sans-serif;
                margin: 0;
                padding: 0;
                background-color: #1a1a1a;
                color: #ddd;
            }

            .header {
                background-color: #111;
                padding: 15px 30px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                color: #fff;
            }

            .header .logo h1 {
                margin: 0;
                font-family: 'Poppins', sans-serif;
                font-size: 26px;
            }

            .header .logo img {
                height: 40px;
                width: auto;
                margin-left: 10px;
            }

            .header .search-bar input {
                padding: 10px;
                width: 350px;
                border-radius: 20px;
                border: 1px solid #444;
                margin-right: 10px;
                font-size: 1em;
                background-color: #333;
                color: white;
            }

            .header .search-bar button {
                padding: 10px 20px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1em;
                color: #fff;
            }

            .nav {
                background-color: #222;
                color: white;
                padding: 15px 0;
            }

            .nav ul {
                display: flex;
                justify-content: center;
                list-style: none;
                margin: 0;
                padding: 0;
            }

            .nav ul li {
                margin: 0 25px;
                cursor: pointer;
            }

            .nav ul li a {
                text-decoration: none;
                color: white;
                font-size: 1.1em;
                transition: color 0.3s;
            }

            .nav ul li a:hover {
                color: #f39c12;
            }

            .contact-section {
                text-align: center;
                padding: 60px 30px;
                background-color: #111;
                margin: 30px 0;
                border-bottom: 5px solid #f39c12;
            }

            .contact-section h2 {
                font-family: 'Gloock', sans-serif;
                font-size: 3.5em;
                color: #f39c12;
                margin-bottom: 20px;
                text-transform: uppercase;
            }

            .contact-section p {
                font-size: 1.1em;
                color: #ccc;
                margin-bottom: 30px;
            }

            .contact-form {
                background-color: #222;
                padding: 40px;
                border-radius: 10px;
                max-width: 800px;
                margin: 0 auto;
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            }

            .contact-form input,
            .contact-form textarea {
                width: 100%;
                padding: 15px;
                margin-bottom: 20px;
                border: 1px solid #444;
                border-radius: 5px;
                background-color: #333;
                color: white;
                font-size: 1em;
            }

            .contact-form button {
                padding: 15px 30px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1.1em;
                color: white;
                width: 100%;
            }

            .contact-form button:hover {
                background-color: #e67e22;
            }

            footer {
                background-color: #111;
                color: white;
                padding: 20px 0;
                text-align: center;
            }

            footer a {
                color: #f39c12;
                text-decoration: none;
                margin: 0 10px;
            }

            footer a:hover {
                text-decoration: underline;
            }
        </style>
    </head>
    <body>
        <header class="header">
            <div class="logo">
                <img src="logo.jpg" alt="logo">
                <h1></h1>
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Search for your favorite dishes...">
                <button>Search</button>
            </div>
        </header>

        <nav class="nav">
            <ul>
                <li><a href="home.html">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="reservation.html">Make a Reservation</a></li>
                <li><a href="contact.html">Contact Us</a></li>
            </ul>
        </nav>

        <section class="contact-section">
            <h2>Contact Us</h2>
            <p>Have questions or feedback? We’d love to hear from you. Get in touch with us today!</p>
            <div class="contact-form">
                <form action="submit-contact.php" method="POST">
                    <label for="name">Full Name:</label>
                    <input type="text" id="name" name="name" required>

                    <label for="email">Email Address:</label>
                    <input type="email" id="email" name="email" required>

                    <label for="subject">Subject:</label>
                    <input type="text" id="subject" name="subject" required>

                    <label for="message">Message:</label>
                    <textarea id="message" name="message" rows="5" required></textarea>

                    <button type="submit">Send Message</button>
                </form>
            </div>
        </section>

        <footer>
            <p>&copy;  | Privacy Policy| Terms & Conditions</p>
        </footer>
    </body>
</html>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Menu -</title>
        <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto:wght@300;400;500&family=Gloock&display=swap" rel="stylesheet">
        <style>
            body {
                font-family: 'Roboto', sans-serif;
                margin: 0;
                padding: 0;
                background-color: #1a1a1a;
                color: #ddd;
            }

            .header {
                background-color: #111;
                padding: 15px 30px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                color: #fff;
            }

            .header .logo h1 {
                margin: 0;
                font-family: 'Poppins', sans-serif;
                font-size: 26px;
            }

            .header .logo img {
                height: 40px;
                width: auto;
                margin-left: 10px;
            }

            .header .search-bar input {
                padding: 10px;
                width: 350px;
                border-radius: 20px;
                border: 1px solid #444;
                margin-right: 10px;
                font-size: 1em;
                background-color: #333;
                color: white;
            }

            .header .search-bar button {
                padding: 10px 20px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1em;
                color: #fff;
            }

            .nav {
                background-color: #222;
                color: white;
                padding: 15px 0;
            }

            .nav ul {
                display: flex;
                justify-content: center;
                list-style: none;
                margin: 0;
                padding: 0;
            }

            .nav ul li {
                margin: 0 25px;
                cursor: pointer;
            }

            .nav ul li a {
                text-decoration: none;
                color: white;
                font-size: 1.1em;
                transition: color 0.3s;
            }

            .nav ul li a:hover {
                color: #f39c12;
            }

            .menu-section {
                text-align: center;
                padding: 60px 30px;
                background-color: #111;
                margin: 30px 0;
                border-bottom: 5px solid #f39c12;
            }

            .menu-section h2 {
                font-family: 'Gloock', sans-serif;
                font-size: 3.5em;
                color: #f39c12;
                margin-bottom: 20px;
                text-transform: uppercase;
            }

            .menu-section p {
                font-size: 1.1em;
                color: #ccc;
                margin-bottom: 30px;
            }

            .menu-items {
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                gap: 20px;
            }

            .menu-item {
                width: 250px;
                background-color: #222;
                padding: 20px;
                text-align: center;
                border-radius: 10px;
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
                border-top: 5px solid #f39c12;
            }

            .menu-item img {
                width: 100%;
                height: 150px;
                object-fit: cover;
                border-radius: 10px;
                margin-bottom: 15px;
            }

            .menu-item h3 {
                font-family: 'Poppins', sans-serif;
                color: #f39c12;
                font-size: 1.5em;
                margin-bottom: 10px;
            }

            .menu-item p {
                color: #ccc;
                font-size: 1.1em;
                margin-bottom: 15px;
            }

            footer {
                background-color: #111;
                color: white;
                padding: 20px 0;
                text-align: center;
            }

            footer a {
                color: #f39c12;
                text-decoration: none;
                margin: 0 10px;
            }

            footer a:hover {
                text-decoration: underline;
            }
        </style>
    </head>
    <body>
        <header class="header">
            <div class="logo">
                <img src="logo.jpg" alt="logo">
                <h1></h1>
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Search for your favorite dishes...">
                <button>Search</button>
            </div>
        </header>

        <nav class="nav">
            <ul>
                <li><a href="home.html">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="admin.html">Admin</a></li>
                <li><a href="reservation.html">Contact Us</a></li>
            </ul>
        </nav>

        <section class="menu-section">
            <h2>Our Menus</h2>
            <p>Discover our exquisite dishes, crafted to bring the finest flavors to your table.</p>
                <!-- Dish 2 -->
                <div class="menu-item">
                    <img src="image/caesar salad.png" alt="download (4)">
                    <h3>Caesar Salad</h3>
                    <p>Fresh romaine lettuce with creamy Caesar dressing, croutons, and parmesan.</p>
                </div>
                <!-- Dish 3 -->
                <div class="menu-item">
                    <img src="image/steak frites.jpg" alt="download (5)">
                    <h3>Steak Frites</h3>
                    <p>Juicy rib-eye steak served with crispy fries and a savory sauce.</p>
                </div>
                <!-- Dish 4 -->
                <div class="menu-item">
                    <img src="image/spaghetticarbonara.jpg" alt="download (5)">
                    <h3>Spaghetti Carbonara</h3>
                    <p>Classic pasta with creamy sauce, crispy pancetta, and parmesan cheese.</p>
                </div>
                <!-- Dish 5 -->
                <div class="menu-item">
                    <img src="image/vegitab;e stir fry.jpg">
                    <h3>Vegetable Stir-fry</h3>
                    <p>Stir-fried seasonal vegetables in a savory soy-based sauce.</p>
                </div>
                <!-- Dish 6 -->
                <div class="menu-item">
                    <img src="image/margherita pizza.jpg" alt="download (7)">
                    <h3>Margherita Pizza</h3>
                    <p>Tomato, fresh mozzarella, and basil on a crispy thin crust.</p>
                </div>
                <!-- Dish 7 -->
                <div class="menu-item">
                    <img src="image/lobser bisque.jpg">
                    <h3>Lobster Bisque</h3>
                    <p>Rich and creamy lobster soup with a hint of brandy and fresh herbs.</p>
                </div>
                <!-- Dish 8 -->
                <div class="menu-item">
                    <img src="image/chicken alfredo.jpg" alt="download (9)">
                    <h3>Chicken Alfredo</h3>
                    <p>Creamy alfredo sauce with tender chicken and fettuccine pasta.</p>
                </div>
                <!-- Dish 9 -->
                <div class="menu-item">
                    <img src="image/beef wellington.jpg" alt="download (10)">
                    <h3>Beef Wellington</h3>
                    <p>Beef tenderloin wrapped in puff pastry with mushroom duxelles and prosciutto.</p>
                </div>
                <!-- Dish 10 -->
                <div class="menu-item">
                    <img src="image/chocolate mousse.jpg" alt="desert">
                    <h3>Chocolate Mousse</h3>
                    <p>Decadent chocolate mousse topped with whipped cream and berries.</p>
                </div>
            </div>
        </section>                                                                                                                              

        <footer>
            <p>&copy; 2024 Velvet Bistro |Privacy Policy | Terms & Conditions</p>
        </footer>
    </body>
</html>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Reservation - Velvet Bistro</title>
        <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto:wght@300;400;500&family=Gloock&display=swap" rel="stylesheet">
        <style>
            body {
                font-family: 'Roboto', sans-serif;
                margin: 0;
                padding: 0;
                background-color: #1a1a1a;
                color: #ddd;
            }

            .header {
                background-color: #111;
                padding: 15px 30px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                color: #fff;
            }

            .header .logo h1 {
                margin: 0;
                font-family: 'Poppins', sans-serif;
                font-size: 26px;
            }

            .header .logo img {
                height: 40px;
                width: auto;
                margin-left: 10px;
            }

            .header .search-bar input {
                padding: 10px;
                width: 350px;
                border-radius: 20px;
                border: 1px solid #444;
                margin-right: 10px;
                font-size: 1em;
                background-color: #333;
                color: white;
            }

            .header .search-bar button {
                padding: 10px 20px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1em;
                color: #fff;
            }

            .nav {
                background-color: #222;
                color: white;
                padding: 15px 0;
            }

            .nav ul {
                display: flex;
                justify-content: center;
                list-style: none;
                margin: 0;
                padding: 0;
            }

            .nav ul li {
                margin: 0 25px;
                cursor: pointer;
            }

            .nav ul li a {
                text-decoration: none;
                color: white;
                font-size: 1.1em;
                transition: color 0.3s;
            }

            .nav ul li a:hover {
                color: #f39c12;
            }

            .reservation-section {
                text-align: center;
                padding: 60px 30px;
                background-color: #111;
                margin: 30px 0;
                border-bottom: 5px solid #f39c12;
            }

            .reservation-section h2 {
                font-family: 'Gloock', sans-serif;
                font-size: 3.5em;
                color: #f39c12;
                margin-bottom: 20px;
                text-transform: uppercase;
            }

            .reservation-section p {
                font-size: 1.1em;
                color: #ccc;
                margin-bottom: 30px;
            }

            .reservation-form {
                background-color: #222;
                padding: 40px;
                border-radius: 10px;
                max-width: 800px;
                margin: 0 auto;
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            }

            .reservation-form input,
            .reservation-form select,
            .reservation-form textarea {
                width: 100%;
                padding: 15px;
                margin-bottom: 20px;
                border: 1px solid #444;
                border-radius: 5px;
                background-color: #333;
                color: white;
                font-size: 1em;
            }

            .reservation-form button {
                padding: 15px 30px;
                background-color: #f39c12;
                border: none;
                cursor: pointer;
                border-radius: 5px;
                font-size: 1.1em;
                color: white;
                width: 100%;
            }

            .reservation-form button:hover {
                background-color: #e67e22;
            }

            footer {
                background-color: #111;
                color: white;
                padding: 20px 0;
                text-align: center;
            }

            footer a {
                color: #f39c12;
                text-decoration: none;
                margin: 0 10px;
            }

            footer a:hover {
                text-decoration: underline;
            }
        </style>
    </head>
    <body>
        <header class="header">
            <div class="logo">
                <img src="logo.jpg" alt="logo">
                <h1></h1>
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Search for your favorite dishes...">
                <button>Search</button>
            </div>
        </header>

        <nav class="nav">
            <ul>
                <li><a href="home.html">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="admin.html">Admin</a></li>
                <li><a href="contact.html">Contact Us</a></li>
            </ul>
        </nav>

        <section class="reservation-section">
            <h2>Make a Reservation</h2>
            <p>Reserve a table and experience a dining experience like no other at Velvet Bistro.</p>
            <div class="reservation-form">
                <form action="submit-reservation.php" method="POST">
                    <label for="name">Full Name:</label>
                    <input type="text" id="name" name="name" required>

                    <label for="email">Email Address:</label>
                    <input type="email" id="email" name="email" required>

                    <label for="phone">Phone Number:</label>
                    <input type="text" id="phone" name="phone" required>

                    <label for="date">Reservation Date:</label>
                    <input type="date" id="date" name="date" required>

                    <label for="time">Reservation Time:</label>
                    <input type="time" id="time" name="time" required>

                    <label for="guests">Number of Guests:</label>
                    <select id="guests" name="guests" required>
                        <option value="1">1</option>
                        <option value="2">2</option>
                        <option value="3">3</option>
                        <option value="4">4</option>
                        <option value="5">5</option>
                        <option value="6">6</option>
                        <option value="7">7</option>
                        <option value="8">8</option>
                        <option value="9">9</option>
                        <option value="10">10</option>
                    </select>

                    <label for="special_requests">Special Requests (optional):</label>
                    <textarea id="special_requests" name="special_requests"></textarea>

                    <button type="submit">Submit Reservation</button>
                </form>
            </div>
        </section>

        <footer>
            <p>&copy; 2024 Velvet Bistro | <a href="privacy.html">Privacy Policy</a> | <a href="terms.html">Terms & Conditions</a></p>
        </footer>
    </body>
</html>
## OUTPUT:
![alt text](<Screenshot 2025-05-29 110318.png>)
![alt text](<Screenshot 2025-05-29 110333.png>)
![alt text](<Screenshot 2025-05-29 110345.png>)
## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
