# Ex04 Places Around Me
# Date: 25/11/2024
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
```
map.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Map</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            text-align: center; /* Centers the content */
            background-color: #b4aeae; /* Optional background color */
        }
        img {
            max-width: 100%; /* Ensures responsiveness */
            height: auto; /* Maintains aspect ratio */
            border: 1px solid #ccc; /* Optional border for the image */
        }
    </style>
    <link rel="icon" href="icon4.png">
</head>
<body>
<br>
<!-- Image with new clickable areas -->
<img src="Imagemap.png" alt="Interactive Map" usemap="#image-map">

<map name="image-map">
    <area alt="Restaurant" title="Vintage Restaurant" href="res.html" coords="53,380,437,532" shape="rect">
    
    <area alt="Supermarket" title="SuperMart" href="market.html" coords="951,267,1189,384" shape="rect">
    <area alt="Auditorium" title="Rentals" href="auditorium.html" coords="577,117,718,114,728,245,557,242,557,237" shape="poly">
</map>

</body>
</html>

res.html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vintage Restaurant</title>
    <link rel="icon" href="icon 1.jpg">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }

        nav {
            padding: 20px;
            background-color: #8cf1a0;
            color: #c00d55;
            display: flex;
            align-items: center;
            flex-wrap: wrap;
            justify-content: space-between;
        }

        nav h1 {
            font-size: 50px;
            margin: 0;
            color: #444;
        }

        nav h3 {
            margin: 5px 20px;
            font-size: 16px;
            color: #333;
        }

        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        nav li {
            display: inline;
            margin: 0 15px;
            color: #555;
            font-weight: bold;
            cursor: pointer;
            transition: color 0.3s;
        }

        nav li:hover {
            color: #c00d55;
        }

        nav .box {
            background-color: #ff7043;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s, transform 0.2s;
        }

        nav .box:hover {
            background-color: #e64a19;
            transform: scale(1.05);
        }

        .searchbar {
            display: flex;
            justify-content: center;
            margin: 30px 0;
        }

        .searchbar input {
            width: 50%;
            padding: 10px;
            border: 2px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
            outline: none;
        }

        .searchbar input:focus {
            border-color: #8cf1a0;
            box-shadow: 0 0 8px rgba(140, 241, 160, 0.5);
        }

        h2 {
            text-align: center;
            font-size: 36px;
            color: #333;
            margin-bottom: 20px;
        }

        .img {
            margin: 20px auto;
            width: 500px;
            padding: 20px;
            border: 2px solid #ccc;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            background-color: #ffffff;
        }

        .img img {
            width: 100%;
            border-radius: 5px;
        }

        .img h3 {
            text-align: center;
            color: #444;
        }

        .img p {
            color: #666;
            font-size: 16px;
            line-height: 1.6;
            text-align: justify;
        }

        .img a {
            display: inline-block;
            margin-top: 10px;
            text-decoration: none;
            color: white;
            background-color: #c00d55;
            padding: 10px 20px;
            border-radius: 5px;
            transition: background-color 0.3s, transform 0.2s;
        }

        .img a:hover {
            background-color: #a30945;
            transform: scale(1.05);
        }

        footer {
            background-color: #333;
            color: #fff;
            padding: 20px 10px;
            text-align: center;
            line-height: 1.6;
        }

        footer .info {
            margin: 20px auto;
            border: 2px dashed #8cf1a0;
            padding: 20px;
            width: fit-content;
        }

        footer p {
            margin: 10px 0;
            color: #ccc;
            font-size: 14px;
        }
    </style>
</head>

<body>
    <nav>
        <div>
            <h1>Vintage Restaurant</h1>
            <h3>Opening Hours 🕥: 10.00 am - 11.00 pm</h3>
        </div>
        <img src="restaurant image 1.jpg" alt="Restaurant" width="150px" height="120px">
        <ul>
            <li>MENU |</li>
            <li>RATINGS |</li>
            <li>BLOG |</li>
            <li>COUPON |</li>
        </ul>
        <a class="box" href="order.html">ORDER NOW!!!</a>
    </nav>

    <div class="searchbar">
        <input placeholder="Search for dishes, offers, or events">
    </div>

    <h2>Food Menu</h2>

    <div class="img">
        <img src="restaurant image 2.jpg" alt="Reservation">
        <h3>Reservation</h3>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corrupti placeat minima recusandae cumque distinctio maiores porro ratione alias minus est praesentium.</p>
        <a href="file:///D:/Web%20Application/Restaurent%20Website/reservation.html">Book Now</a>
    </div>

    <div class="img">
        <img src="restaurant image 4.jpg" alt="Menu">
        <h3>Menu</h3>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eligendi voluptates voluptatem nam tempora eius consequatur nisi error maiores.</p>
        <a href="file:///D:/Web%20Application/Restaurent%20Website/restaurant%20menu.html">View Menu</a>
    </div>

    <div class="img">
        <img src="restaurant image 3.jpg" alt="About Us">
        <h3>About Us</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatum ducimus ratione odit earum esse ullam, magnam perferendis rerum quisquam repellat.</p>
    </div>

    <footer>
        <div>📞 +91 733921961</div>
        <div>🌐 vinatgerestaurent@gmail.com</div>
        <div>📍 Saveetha Nagar, Sriperumbudur</div>
        <div class="info">
            Visit us for an unforgettable dining experience!
        </div>
        <p>&copy; 2024 Vintage Restaurant | All Rights Reserved</p>
    </footer>
</body>

</html>

market.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SuperMart - Your Friendly Supermarket</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: space-around;
            background-color: #333;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 14px 20px;
            display: block;
        }
        nav a:hover {
            background-color: #575757;
        }
        main {
            padding: 20px;
        }
        section {
            margin-bottom: 20px;
        }
        footer {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 10px 20px;
            position: relative;
            bottom: 0;
            width: 100%;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        .grid-item {
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
        }
        .grid-item h3 {
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to SuperMart</h1>
        <p>Your one-stop shop for daily needs!</p>
    </header>
    <nav>
        <a href="#about">About Us</a>
        <a href="#products">Products</a>
        <a href="#contact">Contact</a>
    </nav>
    <main>
        <section id="about">
            <h2>About Us</h2>
            <p>At SuperMart, we aim to provide you with the best products at affordable prices. From fresh produce to household essentials, we have it all.</p>
        </section>
        <section id="products">
            <h2>Our Products</h2>
            <div class="grid">
                <div class="grid-item">
                    <h3>Fruits & Vegetables</h3>
                    <p>Fresh and organic produce straight from the farm.</p>
                </div>
                <div class="grid-item">
                    <h3>Dairy Products</h3>
                    <p>Milk, cheese, and butter of the highest quality.</p>
                </div>
                <div class="grid-item">
                    <h3>Snacks</h3>
                    <p>Chips, biscuits, and chocolates to satisfy your cravings.</p>
                </div>
                <div class="grid-item">
                    <h3>Beverages</h3>
                    <p>Juices, soft drinks, and tea/coffee supplies.</p>
                </div>
                <div class="grid-item">
                    <h3>Household Essentials</h3>
                    <p>Cleaning products, toiletries, and more.</p>
                </div>
            </div>
        </section>
        <section id="contact">
            <h2>Contact Us</h2>
            <p>Email: suppermart@gmail.com</p>
            <p>Phone: 7339219761</p>
            <p>Address: Saveetha Nagar, Sriperumbudur</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 SuperMart. All Rights Reserved.</p>
    </footer>
</body>
</html>

auditorium.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grand Auditorium Rentals</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #283593;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #3949AB;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 14px 20px;
            text-align: center;
        }
        nav a:hover {
            background-color: #5C6BC0;
        }
        main {
            padding: 20px;
        }
        section {
            margin-bottom: 30px;
        }
        footer {
            background-color: #283593;
            color: white;
            text-align: center;
            padding: 10px 20px;
            position: relative;
            bottom: 0;
            width: 100%;
        }
        .services, .pricing {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        .grid-item {
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
        }
        .grid-item h3 {
            margin: 10px 0;
            color: #283593;
        }
        .contact-info {
            font-size: 1.1em;
            line-height: 1.6;
        }
    </style>
</head>
<body>
    <header>
        <h1>Grand Auditorium Rentals</h1>
        <p>Your Perfect Venue for Memorable Events</p>
    </header>
    <nav>
        <a href="#about">About Us</a>
        <a href="#services">Our Services</a>
        <a href="#pricing">Pricing</a>
        <a href="#contact">Contact Us</a>
    </nav>
    <main>
        <section id="about">
            <h2>About Us</h2>
            <p>Welcome to Grand Auditorium Rentals, the ideal destination for hosting your events. With state-of-the-art facilities and spacious seating, we cater to a variety of occasions such as conferences, weddings, concerts, and more.</p>
        </section>
        <section id="services">
            <h2>Our Services</h2>
            <div class="services">
                <div class="grid-item">
                    <h3>Event Management

```
# OUTPUT
![Screenshot 2024-12-08 231149](https://github.com/user-attachments/assets/6101cb2d-30d0-4e7b-be5a-c68c955d19b3)
![Screenshot 2024-12-08 231200](https://github.com/user-attachments/assets/13ef5f7c-8f92-4c97-97e3-b08e97754475)
![Screenshot 2024-12-08 231219](https://github.com/user-attachments/assets/9a4d6764-a9bf-44de-8af3-57cc0922e94f)
![Screenshot 2024-12-08 231229](https://github.com/user-attachments/assets/50f39cec-977c-40d5-a53e-f9fef3617eaa)
![image](https://github.com/user-attachments/assets/a7070c07-a3b6-4f11-b559-9f523611ef79)

# RESULT
The program for implementing image maps using HTML is executed successfully.
