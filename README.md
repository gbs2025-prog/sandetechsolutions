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
        document.addEventListener("DOMContentLoaded", function () {
            let newsTicker = document.getElementById("newsContent");
            newsTicker.innerHTML = `
                🚀 New products and services coming soon! Stay tuned for updates! &nbsp;&nbsp;
                📞 Contact Us at: 0974021114 / 0775506831 / 0961286151 / 0966625837 for all your tech needs! &nbsp;&nbsp;
                🚗 We are located in Lusaka, Chazanga area, along Chalo Bantu Road. Visit us today! &nbsp;&nbsp;
                🎮 Love gaming? Visit us for the best gaming experience in town! &nbsp;&nbsp;
                💈 Need a fresh cut? Come for top-notch barbing services at affordable prices! &nbsp;&nbsp;
                📱 Looking for phone repairs, sales, or accessories? Contact us now! &nbsp;&nbsp;
                ⚡ Speed up your tech with our expert services, from phone repairs to computer lessons! &nbsp;&nbsp;
                🎮 Gaming, barbing, repairs, and more! We’ve got it all! Visit us in Chazanga! &nbsp;&nbsp;
                🚨 For the best tech services and gaming experiences in Lusaka, contact us today! &nbsp;&nbsp;
                💼 We offer: Tech Support, Barbing, Gaming, and more at affordable rates! &nbsp;&nbsp;
                📞 Call us today at 0974021114/0775506831/0961286151/0966625837 for all your needs! &nbsp;&nbsp;
            `;
        });
    </script>
</head>
<body>
    <header>
        <h1>Welcome to Sande Tech Solutions</h1>
    </header>

    <div class="bio">
        <h2>About Sande Tech Solutions</h2>
        <p>Sande Tech Solutions is a leading technology service provider committed to delivering innovative solutions to meet the diverse needs of our clients. We specialize in:</p>
        <ul>
            <li>Software development, including School Management Systems, Hospital Systems, and Stock Inventory Management Systems.</li>
            <li>Tech services such as auditing, tax payments, and computer lessons.</li>
            <li>Phone repairs, sales, and accessories.</li>
            <li>Gaming experiences and barbing services.</li>
        </ul>
        <p>Founded by Sande Tendai, a visionary entrepreneur with a passion for technology and innovation, we aim to revolutionize the tech industry in Lusaka and beyond.</p>
        <h3>Our Mission:</h3>
        <p>To provide high-quality tech solutions that empower businesses, improve services, and enhance everyday life for individuals.</p>
        <h3>Our Vision:</h3>
        <p>To be the go-to technology hub for innovative products, services, and solutions, transforming the tech landscape in Africa.</p>
        <h3>Our Values:</h3>
        <ul>
            <li>Innovation</li>
            <li>Customer Satisfaction</li>
            <li>Integrity</li>
            <li>Excellence</li>
        </ul>
    </div>

    <!-- News Ticker Section -->
    <div id="newsTicker">
        <span id="newsContent"></span>
    </div>
    
<li><a href="sts2.html">Phone Menu</a></li>

    <footer>
        <p>&copy; 2025 Sande Tech Solutions. All rights reserved.</p>
    </footer>
</body>
</html>
