<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Zentrova Order Form</title>

  <style>
    body {
      margin: 0;
      font-family: "Poppins", Arial, sans-serif;
      background: #111;
      color: white;
      padding: 20px;
    }

    h2 {
      text-align: center;
      font-size: 30px;
      margin-bottom: 20px;
    }

    .form-container {
      max-width: 450px;
      margin: auto;
      background: #1d1d1d;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(255,255,255,0.05);
    }

    label {
      font-size: 15px;
      margin-top: 12px;
      display: block;
      font-weight: 500;
    }

    input, select {
      width: 100%;
      padding: 12px;
      margin-top: 5px;
      border-radius: 8px;
      border: none;
      background: #2b2b2b;
      color: white;
      font-size: 15px;
    }

    button {
      width: 100%;
      margin-top: 20px;
      padding: 15px;
      background: #00c853;
      border: none;
      color: white;
      font-size: 18px;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
      box-shadow: 0 0 10px rgba(0, 200, 83, 0.5);
    }

    button:hover {
      background: #00e676;
      transform: scale(1.03);
    }
  </style>
</head>
<body>

  <h2>🛒 Zentrova Order Form</h2>

  <div class="form-container">
    
    <label>Product Name</label>
    <input id="product" type="text" placeholder="Enter product name">

    <label>Size</label>
    <input id="size" type="text" placeholder="M / L / XL etc">

    <label>Your Name</label>
    <input id="customer" type="text" placeholder="Your full name">

    <label>Phone Number</label>
    <input id="phone" type="number" placeholder="10-digit mobile">

    <label>State</label>
    <input id="state" type="text" placeholder="Your state">

    <label>City</label>
    <input id="city" type="text" placeholder="Your city">

    <label>Village</label>
    <input id="village" type="text" placeholder="Village / Area">

    <label>Pincode</label>
    <input id="pincode" type="number" placeholder="6-digit pincode">

    <label>Payment Method</label>
    <select id="payment">
      <option value="COD">Cash On Delivery</option>
      <option value="Online">Online Payment</option>
    </select>

    <button onclick="sendWhatsApp()">Send to WhatsApp</button>

  </div>

<script>
function sendWhatsApp() {
  let msg =
`🚨⚠️ Alert Zentrova New Order Details

Product Name: ${document.getElementById('product').value}
Size: ${document.getElementById('size').value}

Customer Name: ${document.getElementById('customer').value}
Phone: ${document.getElementById('phone').value}

State: ${document.getElementById('state').value}
City: ${document.getElementById('city').value}
Village: ${document.getElementById('village').value}
Pincode: ${document.getElementById('pincode').value}

Payment Method: ${document.getElementById('payment').value}`;

  let phone = "9332307996";

  let url = `https://wa.me/${phone}?text=${encodeURIComponent(msg)}`;

  window.open(url, "_blank");
}
</script>

</body>
</html>
