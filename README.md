<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sande Tech Solutions</title>
    <style>
        body {
            background: linear-gradient(to right, black, purple);
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        header {
            padding: 20px;
        }
        img {
            max-width: 300px;
        }
        .content {
            padding: 50px;
        }
        select, button, textarea {
            padding: 10px;
            margin: 10px;
            font-size: 16px;
            border-radius: 5px;
            border: none;
        }
        button {
            background: white;
            color: black;
            cursor: pointer;
        }
        button:hover {
            background: lightgray;
        }
        .bio {
            padding: 50px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            margin: 20px;
        }
        footer {
            padding: 20px;
            margin-top: 50px;
            background: rgba(255, 255, 255, 0.2);
        }
        #confirmationMessage {
            display: none;
            background: green;
            color: white;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
        }
        #newsTicker {
            width: 100%;
            overflow: hidden;
            white-space: nowrap;
            background: rgba(255, 255, 255, 0.2);
            color: yellow;
            padding: 10px 0;
            font-size: 18px;
            position: fixed;
            bottom: 0;
            left: 0;
        }
        @keyframes scrollText {
            from { transform: translateX(100%); }
            to { transform: translateX(-100%); }
        }
        #newsContent {
            display: inline-block;
            animation: scrollText 10s linear infinite;
        }
    </style>
    <script>
        const prices = {
            "Product 1": 150,
            "Product 2": 200,
            "Product 3": 300,
            "School System": 400,
            "Hospital System": 500,
            "Pharmacy System": 450,
            "Stock Inventory System": 350,
            "iPhones Available": 1000,
            "Pouches": 50,
            "Headsets": 100,
            "Tendai Sande Books": 250,
            "Beats": 500,
            "Service 1": 250,
            "Service 2": 350,
            "Service 3": 500,
            "Auditing": 400,
            "Tax Payments": 300,
            "Phone or Computer Screen Replacement": 200,
            "Phone and Computer Charging": 50,
            "Barbing": 100,
            "Computer Lessons": 150
        };

        function updatePrice() {
            let product = document.getElementById("product").value;
            let service = document.getElementById("service").value;
            let priceDisplay = document.getElementById("price");
            
            if (product !== "none") {
                priceDisplay.innerText = "Price: " + prices[product] + " ZMW";
                document.getElementById("service").value = "none";
            } else if (service !== "none") {
                priceDisplay.innerText = "Price: " + prices[service] + " ZMW";
                document.getElementById("product").value = "none";
            } else {
                priceDisplay.innerText = "";
            }
        }

        function purchase() {
            let product = document.getElementById("product").value;
            let service = document.getElementById("service").value;
            let confirmationMessage = document.getElementById("confirmationMessage");
            
            if (product === "none" && service === "none") {
                alert("Please select a product or service before making a purchase.");
                return;
            }

            let selectedItem = product !== "none" ? product : service;
            confirmationMessage.innerText = "Thank you for purchasing " + selectedItem + "!";
            confirmationMessage.style.display = "block";
        }
    </script>
</head>
<body>
    <header>
        <img src="sts.png.webp" alt="Sande Tech Solutions Logo">
        <h1>Welcome to Sande Tech Solutions</h1>
    </header>
    
    <div class="content">
        <h2>Select Your Product or Service</h2>
        
        <label for="product">Choose a product:</label>
        <select id="product" onchange="updatePrice()">
            <option value="none">-- Select Product --</option>
            <option value="Product 1">Product 1 - Description</option>
            <option value="Product 2">Product 2 - Description</option>
            <option value="Product 3">Product 3 - Description</option>
            <option value="School System">School Management System</option>
            <option value="Hospital System">Hospital Management System</option>
            <option value="Pharmacy System">Pharmacy Management System</option>
            <option value="Stock Inventory System">Stock Inventory Management System</option>
            <option value="iPhones Available">All iPhones Available</option>
            <option value="Pouches">Pouches</option>
            <option value="Headsets">Headsets</option>
            <option value="Tendai Sande Books">Tendai Sande Books</option>
            <option value="Beats">Beats</option>
        </select>
        
        <label for="service">Choose a service:</label>
        <select id="service" onchange="updatePrice()">
            <option value="none">-- Select Service --</option>
            <option value="Auditing">Auditing</option>
            <option value="Tax Payments">Tax Payments</option>
            <option value="Phone or Computer Screen Replacement">Phone/Computer Screen Replacement</option>
            <option value="Phone and Computer Charging">Phone/Computer Charging</option>
            <option value="Barbing">Barbing</option>
            <option value="Computer Lessons">Computer Lessons</option>
        </select>
        
        <h3 id="price" style="color: yellow;"></h3>
        
        <h2>Leave a Suggestion or Comment</h2>
        <textarea id="comment" rows="4" cols="50" placeholder="Enter your suggestion or feedback here..."></textarea>
        
        <button onclick="purchase()">Make Purchase</button>
        
        <div id="confirmationMessage"></div>
    </div>

    <div id="newsTicker">
        <span id="newsContent">New products and services coming soon! Stay tuned for updates!</span>
    </div>

    <div class="bio">
        <h2>Who is Sande Tendai?</h2>
        <img src="tendaisandesite.jpeg" style="max-width: 1000px; border-radius: 100px;">
        <p>Sande Tendai is a visionary entrepreneur and technology enthusiast dedicated to providing innovative tech solutions tailored to modern business needs. With years of experience in the tech industry, Sande specializes in cutting-edge digital solutions, helping businesses transform and thrive in the digital age. Passionate about innovation, technology, and Africa’s growing digital economy, Sande is committed to bridging the gap between technology and business efficiency.</p>
    </div>
    

        
            <li><a href="sts22025.html"> link to phone Services</a></li>
           
    
    <footer>
        <p>&copy; 2025 Sande Tech Solutions. All rights reserved.</p>
    </footer>
</body>
</html>
