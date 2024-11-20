<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Borrow App - Login</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #e8f5e9;
      margin: 0;
      padding: 0;
    }

    .container {
      width: 100%;
      max-width: 400px;
      margin: 100px auto;
      background-color: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0px 0px 15px rgba(0, 128, 0, 0.1);
      text-align: center;
    }

    h1 {
      color: #2e7d32;
      margin-bottom: 20px;
    }

    input {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      width: 100%;
      padding: 10px;
      background-color: #2e7d32;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background-color: #1b5e20;
    }

    .error {
      color: red;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Login to Borrow App</h1>
    <input type="text" id="username" placeholder="Username" required />
    <input type="password" id="password" placeholder="Password" required />
    <button onclick="login()">Login</button>
    <p class="error" id="error-message"></p>
  </div>

  <script>
    // Predefined credentials
    const validUsername = "somesh";
    const validPassword = "Someshwar@3032";

    function login() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;
      const errorMessage = document.getElementById("error-message");

      // Validate credentials
      if (username === validUsername && password === validPassword) {
        alert("Login successful! Redirecting to the dashboard...");
        // Redirect to dashboard or another page after successful login
        window.location.href = "dashboard.html"; // Example: redirect to dashboard page
      } else {
        errorMessage.textContent = "Invalid username or password. Please try again.";
      }
    }
  </script>

</body>
</html>
