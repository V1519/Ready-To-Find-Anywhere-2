<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ready To Find Here</title>
  <!-- Linking external Font Awesome icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
  <!-- Internal CSS for styles -->
  <style>
    /* General Reset and Styling */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
    }

    /* Glass effect container */
    .glass-container {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 100%;
    }

    /* Login popup styles */
    .login-box {
      background: rgba(255, 255, 255, 0.9);
      padding: 30px 40px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      color: black;
      text-align: center;
      width: 100%;
      max-width: 400px;
    }

    h2 {
      margin-bottom: 15px;
      font-size: 24px;
    }

    /* Login form styles */
    form input[type="text"],
    form input[type="password"] {
      margin: 10px 0;
      padding: 10px;
      width: 100%;
      border: 1px solid #717171;
      border-radius: 5px;
      font-size: 14px;
    }

    button[type="submit"] {
      margin: 15px 0;
      padding: 10px;
      background-color: #1e90ff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      width: 100%;
    }

    button[type="submit"]:hover {
      background-color: #1c7ed6;
    }

    /* Success Section */
    .container {
      display: none;
      text-align: center;
      color: white;
      font-size: 1.2em;
      padding: 20px;
      background: rgba(0, 0, 0, 0.7);
      width: 100%;
      height: 100vh;
      justify-content: center;
      align-items: center;
      position: fixed;
      flex-direction: column;
    }

    .links {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 10px 0;
    }

    .folder {
      margin: 10px 0;
      display: flex;
      align-items: center;
      background-color: #2e2e2e;
      padding: 10px;
      border-radius: 8px;
      width: 250px;
      text-decoration: none;
      color: white;
      transition: background-color 0.3s ease;
    }

    .folder:hover {
      background-color: #3d3d3d;
    }

    .folder i {
      margin-right: 8px;
    }

    footer {
      position: absolute;
      bottom: 10px;
      font-size: 12px;
      color: #aaaaaa;
    }
  </style>
</head>

<body>
  <!-- Login Section -->
  <div class="glass-container">
    <div class="login-box" id="loginContainer">
      <h2>Ready To Find Here</h2>
      <form id="loginForm">
        <input type="text" id="username" name="username" required placeholder="Username" />
        <input type="password" id="password" name="password" required placeholder="Password" />
        <button type="submit">Login</button>
        <p id="message" style="color: red; display: none;"></p>
      </form>
    </div>
  </div>

  <!-- Success Page Section -->
  <div class="container" id="successPage">
    <h2>Welcome Mr. Viraj Rajendra Gite</h2>
    <div class="links">
      <a class="folder" href="https://drive.google.com/drive/folders/1-wrFpLpvqZVeaSLi1NE9LkWmxWRM1Z-3?usp=sharing" target="_blank">
        <i class="fab fa-google-drive"></i> C.V. Otur
      </a>
      <a class="folder" href="https://drive.google.com/drive/folders/1T8JubDmOVCGtesj8PNx5hvEO1Th_cXS9?usp=sharing" target="_blank">
        <i class="fab fa-google-drive"></i> Important
      </a>
      <a class="folder" href="https://drive.google.com/drive/folders/14_AuX_uppE5GAaVUkxv2hQhqbVAoF5t8?usp=sharing" target="_blank">
        <i class="fab fa-google-drive"></i> Tour
      </a>
      <a class="folder" href="https://drive.google.com/drive/folders/1zX9ExampleLink12345" target="_blank">
        <i class="fab fa-google-drive"></i> My Family
      </a>
    </div>
  </div>

  <footer>Created by Mr. Viraj Rajendra Gite</footer>

  <script>
    const validCredentials = { 'virajgite32@gmail.com': 'viraj@234632' };
    const loginForm = document.getElementById('loginForm');
    const loginContainer = document.getElementById('loginContainer');
    const successPage = document.getElementById('successPage');
    const messageEl = document.getElementById('message');

    loginForm.addEventListener('submit', function (e) {
      e.preventDefault();
      const username = document.getElementById('username').value.trim();
      const password = document.getElementById('password').value;

      if (validCredentials[username] === password) {
        loginContainer.style.display = 'none';
        successPage.style.display = 'flex';
      } else {
        messageEl.textContent = 'Invalid credentials';
        messageEl.style.display = 'block';
      }
    });
  </script>
</body>

</html>
