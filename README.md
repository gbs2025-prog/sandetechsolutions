<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sande Tech Solutions</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <style>
        body {
            background: linear-gradient(to right, black, purple);
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .content, .bio {
            padding: 20px;
        }
        select, button, textarea, input {
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
        #confirmationMessage {
            display: none;
            background: green;
            color: white;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
        }
        /* News Ticker Styles */
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
        #newsContent {
            display: inline-block;
            white-space: nowrap;
            padding-left: 100%;
            animation: scrollText 10s linear infinite;
        }
        @keyframes scrollText {
            from { transform: translateX(100%); }
            to { transform: translateX(-100%); }
        }
    </style>
    <script>
        function generateReceipt() {
            const { jsPDF } = window.jspdf;
            let doc = new jsPDF();
            let product = document.getElementById("product").value;
            let service = document.getElementById("service").value;
            let email = document.getElementById("email").value;
            let selectedItem = product !== "none" ? product : service;
            
            if (selectedItem === "none") {
                alert("Please select a product or service before proceeding.");
                return;
            }
            
            doc.text("Sande Tech Solutions Receipt", 10, 10);
            doc.text("Product/Service: " + selectedItem, 10, 20);
            doc.text("Thank you for your purchase!", 10, 30);
            
            doc.save("receipt.pdf");
            document.getElementById("confirmationMessage").innerText = "Receipt generated for " + selectedItem;
            document.getElementById("confirmationMessage").style.display = "block";
        }

        document.addEventListener("DOMContentLoaded", function () {
            let newsTicker = document.getElementById("newsContent");
            newsTicker.innerHTML = "🚀 New products and services coming soon! Stay tuned for updates! ";
        });
    </script>
</head>
<body>
    <header>
        <h1>Welcome to Sande Tech Solutions</h1>
    </header>
    
    <div class="content">
        <h2>Select Your Product or Service</h2>
        <label for="product">Choose a product:</label>
        <select id="product">
            <option value="none">-- Select Product --</option>
            <option value="School System">School Management System</option>
            <option value="Hospital System">Hospital Management System</option>
            <option value="Stock Inventory System">Stock Inventory System</option>
        </select>
        <label for="service">Choose a service:</label>
        <select id="service">
            <option value="none">-- Select Service --</option>
            <option value="Auditing">Auditing</option>
            <option value="Tax Payments">Tax Payments</option>
            <option value="Computer Lessons">Computer Lessons</option>
        </select>
        <br>
        <label for="email">Enter your Email:</label>
        <input type="email" id="email" placeholder="Enter your email">
        <br>
        <button onclick="generateReceipt()">Generate Receipt</button>
        <div id="confirmationMessage"></div>
    </div>

    <!-- News Ticker Section -->
    <div id="newsTicker">
        <span id=" 📞 Contact Us at: 0974021114 / 0775506831 / 0961286151 / 0966625837 for all your tech needs! 🚗 We are located in Lusaka, Chazanga area, along Chalo Bantu Road. Visit us today! 🎮 Love gaming? Visit us for the best gaming experience in town! 💈 Need a fresh cut? Come for top-notch barbing services at affordable prices! 📱 Looking for phone repairs, sales, or accessories? Contact us now! ⚡ Speed up your tech with our expert services, from phone repairs to computer lessons! 🎮 Gaming, barbing, repairs, and more! We’ve got it all! Visit us in Chazanga! 🚨 For the best tech services and gaming experiences in Lusaka, contact us today!💼 We offer: Tech Support, Barbing, Gaming, and more at affordable rates!📞 Call us today at 0974021114/0775506831/0961286151/0966625837 for all your needs!"></span>
    </div>

    <div class="bio">
        <h2>Who is Sande Tendai?</h2>
        <p>Sande Tendai is a visionary entrepreneur dedicated to providing innovative tech solutions.</p>
    </div>
    
    <li><a href="sts2.html">Phone Menu</a></li>
    
    <footer>
        <p>&copy; 2025 Sande Tech Solutions. All rights reserved.</p>
    </footer>
</body>
</html>
