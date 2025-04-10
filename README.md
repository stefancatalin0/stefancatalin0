<!DOCTYPE html>
<html lang="ro">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Facebook Login</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Helvetica, Arial, sans-serif;
      background-color: #f0f2f5;
    }

    .fb-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      padding: 20px;
    }

    .fb-left {
      flex: 1;
      max-width: 500px;
      padding-right: 50px;
    }

    .fb-left h1 {
      color: #1877f2;
      font-size: 60px;
      margin-bottom: 10px;
    }

    .fb-left p {
      font-size: 24px;
      color: #1c1e21;
    }

    .fb-right {
      background: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      width: 360px;
      text-align: center;
    }

    .fb-login-form input {
      width: 100%;
      padding: 14px;
      margin-bottom: 12px;
      border: 1px solid #dddfe2;
      border-radius: 6px;
      font-size: 17px;
    }

    .fb-login-form button {
      width: 100%;
      padding: 14px;
      background-color: #1877f2;
      color: white;
      border: none;
      border-radius: 6px;
      font-size: 20px;
      font-weight: bold;
      cursor: pointer;
      margin-bottom: 12px;
    }

    .fb-login-form a {
      display: block;
      margin-bottom: 12px;
      color: #1877f2;
      font-size: 14px;
      text-decoration: none;
    }

    hr {
      margin: 20px 0;
      border: none;
      border-top: 1px solid #dddfe2;
    }

    .create-account {
      background-color: #42b72a;
      font-size: 17px;
      padding: 12px;
      font-weight: bold;
    }

    .create-page {
      font-size: 14px;
      color: #1c1e21;
      margin-top: 20px;
    }

    .create-page a {
      font-weight: bold;
      color: #1c1e21;
      text-decoration: none;
    }

    .error-msg {
      color: red;
      margin-top: 10px;
      font-size: 14px;
    }

    .success-msg {
      color: green;
      margin-top: 10px;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <div class="fb-container">
    <div class="fb-left">
      <h1>facebook</h1>
      <p>Facebook te ajută să comunici și să intri în contact cu persoanele din viața ta.</p>
    </div>
    <div class="fb-right">
      <form class="fb-login-form" id="loginForm">
        <input type="text" id="email" placeholder="Adresă de email sau număr de telefon" required>
        <input type="password" id="password" placeholder="Parolă" required>
        <button type="submit">Conectează-te</button>
        <p id="errorMsg"></p>
        <a href="#">Ai uitat parola?</a>
        <hr>
        <button type="button" class="create-account">Creează un cont nou</button>
      </form>
      <p class="create-page"><a href="#">Creează o pagină</a> pentru o celebritate, un brand sau o afacere.</p>
    </div>
  </div>

  <script>
    document.getElementById("loginForm").addEventListener("submit", function (e) {
      e.preventDefault();

      const email = document.getElementById("email").value.trim();
      const password = document.getElementById("password").value.trim();
      const errorMsg = document.getElementById("errorMsg");

      // Date valide simulate
      const validEmail = "admin@demo.com";
      const validPassword = "1234";

      if (email === validEmail && password === validPassword) {
        errorMsg.textContent = "Autentificare reușită!";
        errorMsg.className = "success-msg";
        // redirect simulat:
        // window.location.href = "profil.html";
      } else {
        errorMsg.textContent = "Email sau parolă greșită!";
        errorMsg.className = "error-msg";
      }
    });
  </script>
</body>
</html>
