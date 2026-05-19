<!DOCTYPE html>
<html>
<head>
    <title>Manaswini Hospitals</title>

    <style>
        body {
            font-family: 'Segoe UI', sans-serif;
            margin: 0;
            background: linear-gradient(135deg, #e6f0ff, #f9fcff);
        }

        header {
            background: linear-gradient(90deg, #0a74da, #00c6ff);
            color: white;
            padding: 30px;
            text-align: center;
        }

        .logo {
            width: 120px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            margin-bottom: 10px;
        }

        nav {
            background: white;
            padding: 10px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        nav a {
            color: #0a74da;
            margin: 15px;
            text-decoration: none;
            font-weight: bold;
        }

        .container {
            padding: 20px;
        }

        .card {
            background: white;
            padding: 20px;
            margin: 20px 0;
            border-radius: 12px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
        }

        h2 {
            color: #0a74da;
            border-bottom: 2px solid #0a74da;
            padding-bottom: 5px;
        }

        button {
            background: #0a74da;
            color: white;
            padding: 12px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
        }

        button:hover {
            background: #005bb5;
        }

        footer {
            background: #0a74da;
            color: white;
            text-align: center;
            padding: 15px;
        }
    </style>
</head>

<body>

<header>
    <img src="logo.png" class="logo">
    <h1>Manaswini Hospitals</h1>
    <p>Advanced Care | Trusted Doctors | 24/7 Service</p>
</header>

<nav>
    <a href="#">Home</a>
    <a href="#">Services</a>
    <a href="#">Doctors</a>
    <a href="#">Contact</a>
</nav>

<div class="container">

    <div class="card">
        <h2>About Us</h2>
        <p>Manaswini Hospitals provides high-quality healthcare with modern technology and expert doctors.</p>
    </div>

    <div class="card">
        <h2>Our Services</h2>
        <ul>
            <li>General Medicine</li>
            <li>Emergency Care</li>
            <li>Lab Tests</li>
            <li>Pharmacy</li>
        </ul>
    </div>

    <div class="card">
        <h2>Our Doctors</h2>

        <h3>Dr. Suman Bandi</h3>
        <p>M.D. | Professor of General Medicine</p>

        <hr>

        <h3>Dr. Shiva Kumar</h3>
        <p>MBBS</p>
    </div>

    <div class="card">
        <h2>Management</h2>
        <h3>A. Raju</h3>
        <p>Managing Head</p>
    </div>

    <div class="card">
        <h2>Working Hours</h2>
        <p>🕒 24/7 Available</p>
    </div>

    <div class="card">
        <h2>Book Appointment</h2>

        <form onsubmit="sendToWhatsApp(); return false;">
            <input type="text" id="name" placeholder="Your Name" required><br><br>
            <input type="tel" id="phone" placeholder="Phone Number" required><br><br>
            <input type="date" id="date" required><br><br>

            <select id="department">
                <option>General Medicine</option>
                <option>Emergency</option>
                <option>Lab Test</option>
            </select><br><br>

            <button type="submit">Book via WhatsApp</button>
        </form>
    </div>

    <div class="card">
        <h2>Contact</h2>
        <p>📞 <a href="tel:9948550546">9948550546</a></p>
        <p>📍 Opposite Vandana Nursing Home, beside Mamatha Maternity and Children Nursing Home, Narsampet, Telangana 506132</p>
    </div>

    <div class="card">
        <h2>Find Us on Map</h2>

        <iframe 
        src="https://www.google.com/maps?q=Narsampet,Telangana&output=embed"
        width="100%" height="300" style="border:0; border-radius:10px;">
        </iframe>

    </div>

</div>

<footer>
    <p>© 2026 Manaswini Hospitals</p>
</footer>

<script>
function sendToWhatsApp() {
    var name = document.getElementById("name").value;
    var phone = document.getElementById("phone").value;
    var date = document.getElementById("date").value;
    var dept = document.getElementById("department").value;

    var message = "Appointment Request:%0A"
        + "Name: " + name + "%0A"
        + "Phone: " + phone + "%0A"
        + "Date: " + date + "%0A"
        + "Department: " + dept;

    var url = "https://wa.me/919948550546?text=" + message;

    window.open(url, "_blank");
}
</script>

</body>
</html>
